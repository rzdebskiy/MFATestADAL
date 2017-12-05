# XamarinFormsMFASample
Sample and step by step guide of integrating Multi-Factor Authentication in Xamarin Forms iOS/Android/UWP app using Active Directory Authentication Library (ADAL).
Sample is based on [Dependency Service ADAL Sample in Xamarin Blog](https://blog.xamarin.com/put-adal-xamarin-forms/), Windows Phone Silverlight implementation replaced with UWP. 

# Step by Step Guide

1. Login to your [Azure Subscription](https://portal.azure.com/) or [start free trial](https://azure.microsoft.com/en-us/offers/ms-azr-0044p)
2. Activate [Azure Active Directory Premium free trial](https://azure.microsoft.com/en-us/trial/get-started-active-directory/) or purchase [Azure Active Directory Premium](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-get-started-premium)/[Enterprise Mobility + Security](https://www.microsoft.com/en-us/cloud-platform/enterprise-mobility-security) - this is needed to have Multi-Factor Authentication functionality available for your account. 
2. Create Azure Active Directory [tenant and test user with enabled multi-factor authentication](https://docs.microsoft.com/en-us/rest/api/datacatalog/create-an-azure-active-directory-tenant).
3. [Register your application](https://docs.microsoft.com/en-us/rest/api/datacatalog/register-a-client-app) in Azure Active Directroy to get Client ID.
4. Insert Client ID (Application ID) into [MainPage.xaml.cs](MFATest/MFATest/MainPage.xaml.cs#L13)

`public static string clientId = "INSERT YOUR CLIENT ID HERE";`

5. Change returnUri in [MainPage.xaml.cs](MFATest/MFATest/MainPage.xaml.cs#L15) to valid URI you have configured in Azure Active Directory App Registration or use existing one from this sample (ensure you configure the same in Azure AD the portal):

`public static string returnUri = "http://MFATestPCL-redirect";`

Screenshots on how it works:

# iOS:

<p align="center">
<img src="img/iOS_MFA_1.jpg" width="150"/>
<img src="img/iOS_MFA_2.jpg" width="150"/>
<img src="img/iOS_MFA_3.jpg" width="150"/>
<img src="img/iOS_MFA_4.jpg" width="150"/>
<img src="img/iOS_MFA_5.jpg" width="150"/>
</p>

# Android:

<p align="center">
<img src="img/Android_MFA_1.png" width="150"/>
<img src="img/Android_MFA_2.png" width="150"/>
<img src="img/Android_MFA_3.png" width="150"/>
<img src="img/Android_MFA_4.png" width="150"/>
<img src="img/Android_MFA_5.png" width="150"/>
</p>

