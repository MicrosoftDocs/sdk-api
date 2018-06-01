---
UID: NF:adshlp.ADsOpenObject
title: ADsOpenObject function
author: windows-sdk-content
description: Binds to an ADSI object using explicit user name and password credentials.
old-location: adsi\adsopenobject.htm
old-project: ADSI
ms.assetid: c4b85d8e-b33b-47a4-b7d7-5f901f80dce9
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ADsOpenObject, ADsOpenObject function [ADSI], _ds_adsopenobject, adshlp/ADsOpenObject, adsi.adsopenobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	DllExport
 - HeaderDef
: 
api_location:
-	Activeds.dll
 - accctrl.h
: 
api_name:
-	ADsOpenObject
 - _ACCESS_MODE
: 
product: Windows
targetos: Windows
 - _MULTIPLE_TRUSTEE_OPERATION
: 
 - _PROGRESS_INVOKE_SETTING
: 
 - _SE_OBJECT_TYPE
: 
 - _TRUSTEE_FORM
: 
 - _TRUSTEE_TYPE
: 
req.lib: Activeds.lib
req.dll: Activeds.dll
 - _ACTRL_ACCESS_ENTRYA
: 
 - _ACTRL_ACCESS_ENTRYW
: 
 - _ACTRL_ACCESS_ENTRY_LISTA
: 
 - _ACTRL_ACCESS_ENTRY_LISTW
: 
 - _ACTRL_ALISTA
: 
 - _ACTRL_ALISTW
: 
 - _ACTRL_PROPERTY_ENTRYA
: 
 - _ACTRL_PROPERTY_ENTRYW
: 
 - _EXPLICIT_ACCESS_A
: 
 - _EXPLICIT_ACCESS_W
: 
 - _INHERITED_FROMA
: 
 - _INHERITED_FROMW
: 
 - _OBJECTS_AND_NAME_A
: 
 - _OBJECTS_AND_NAME_W
: 
 - _OBJECTS_AND_SID
: 
 - _TRUSTEE_A
: 
 - _TRUSTEE_W
: 
req.irql: 
 - 
: 
 - BuildExplicitAccessWithNameA
: 
 - BuildExplicitAccessWithNameW
: 
 - BuildSecurityDescriptorA
: 
 - BuildSecurityDescriptorW
: 
 - BuildTrusteeWithNameA
: 
 - BuildTrusteeWithNameW
: 
 - BuildTrusteeWithObjectsAndNameA
: 
 - BuildTrusteeWithObjectsAndNameW
: 
 - BuildTrusteeWithObjectsAndSidA
: 
 - BuildTrusteeWithObjectsAndSidW
: 
 - BuildTrusteeWithSidA
: 
 - BuildTrusteeWithSidW
: 
 - FreeInheritedFromArray
: 
 - GetAuditedPermissionsFromAclA
: 
 - GetAuditedPermissionsFromAclW
: 
 - GetEffectiveRightsFromAclA
: 
 - GetEffectiveRightsFromAclW
: 
 - GetExplicitEntriesFromAclA
: 
 - GetExplicitEntriesFromAclW
: 
 - GetInheritanceSourceA
: 
 - GetInheritanceSourceW
: 
 - GetNamedSecurityInfoA
: 
 - GetNamedSecurityInfoW
: 
 - GetSecurityInfo
: 
 - GetTrusteeFormA
: 
 - GetTrusteeFormW
: 
 - GetTrusteeNameA
: 
 - GetTrusteeNameW
: 
 - GetTrusteeTypeA
: 
 - GetTrusteeTypeW
: 
 - LookupSecurityDescriptorPartsA
: 
 - LookupSecurityDescriptorPartsW
: 
 - SetEntriesInAclA
: 
 - SetEntriesInAclW
: 
 - SetNamedSecurityInfoA
: 
 - SetNamedSecurityInfoW
: 
 - SetSecurityInfo
: 
 - TreeResetNamedSecurityInfoA
: 
 - TreeResetNamedSecurityInfoW
: 
 - TreeSetNamedSecurityInfoA
: 
 - TreeSetNamedSecurityInfoW
: 
 - aclui.h
: 
 - _SI_PAGE_TYPE
: 
 - CreateSecurityPage
: 
 - EditSecurity
: 
 - EditSecurityAdvanced
: 
 - _EFFPERM_RESULT_LIST
: 
 - _SECURITY_OBJECT
: 
 - _SID_INFO
: 
 - _SID_INFO_LIST
: 
 - _SI_ACCESS
: 
 - _SI_INHERIT_TYPE
: 
 - _SI_OBJECT_INFO
: 
 - COM
: 
 - activation.h
: 
 - IActivationFactory.ActivateInstance
: 
 - IActivationFactory
: 
 - activationregistration.h
: 
 - ActivationType
: 
 - IdentityType
: 
 - InstancingType
: 
 - RegistrationScope
: 
 - ThreadingType
: 
 - IActivatableClassRegistration
: 
 - IDllServerActivatableClassRegistration
: 
 - IExeServerActivatableClassRegistration
: 
 - IExeServerRegistration
: 
 - adhoc.h
: 
 - tagDOT11_ADHOC_AUTH_ALGORITHM
: 
 - tagDOT11_ADHOC_CIPHER_ALGORITHM
: 
 - tagDOT11_ADHOC_CONNECT_FAIL_REASON
: 
 - tagDOT11_ADHOC_NETWORK_CONNECTION_STATUS
: 
 - IDot11AdHocInterface.GetActiveNetwork
: 
 - IDot11AdHocInterface.GetDeviceSignature
: 
 - IDot11AdHocInterface.GetFriendlyName
: 
 - IDot11AdHocInterface.GetIEnumDot11AdHocNetworks
: 
 - IDot11AdHocInterface.GetIEnumSecuritySettings
: 
 - IDot11AdHocInterface.GetStatus
: 
 - IDot11AdHocInterface.IsAdHocCapable
: 
 - IDot11AdHocInterface.IsDot11d
: 
 - IDot11AdHocInterface.IsRadioOn
: 
 - IDot11AdHocInterfaceNotificationSink.OnConnectionStatusChange
: 
 - IDot11AdHocManager.CommitCreatedNetwork
: 
 - IDot11AdHocManager.CreateNetwork
: 
 - IDot11AdHocManager.GetIEnumDot11AdHocInterfaces
: 
 - IDot11AdHocManager.GetIEnumDot11AdHocNetworks
: 
 - IDot11AdHocManager.GetNetwork
: 
 - IDot11AdHocManagerNotificationSink.OnInterfaceAdd
: 
 - IDot11AdHocManagerNotificationSink.OnInterfaceRemove
: 
 - IDot11AdHocManagerNotificationSink.OnNetworkAdd
: 
 - IDot11AdHocManagerNotificationSink.OnNetworkRemove
: 
 - IDot11AdHocNetwork.Connect
: 
 - IDot11AdHocNetwork.DeleteProfile
: 
 - IDot11AdHocNetwork.Disconnect
: 
 - IDot11AdHocNetwork.GetContextGuid
: 
 - IDot11AdHocNetwork.GetInterface
: 
 - IDot11AdHocNetwork.GetProfileName
: 
 - IDot11AdHocNetwork.GetSecuritySetting
: 
 - IDot11AdHocNetwork.GetSignalQuality
: 
 - IDot11AdHocNetwork.GetSignature
: 
 - IDot11AdHocNetwork.GetSSID
: 
 - IDot11AdHocNetwork.GetStatus
: 
 - IDot11AdHocNetwork.HasProfile
: 
 - IDot11AdHocNetworkNotificationSink.OnConnectFail
: 
 - IDot11AdHocNetworkNotificationSink.OnStatusChange
: 
 - IDot11AdHocSecuritySettings.GetDot11AuthAlgorithm
: 
 - IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm
: 
 - IEnumDot11AdHocInterfaces.Clone
: 
 - IEnumDot11AdHocInterfaces.Next
: 
 - IEnumDot11AdHocInterfaces.Reset
: 
 - IEnumDot11AdHocInterfaces.Skip
: 
 - IEnumDot11AdHocNetworks.Clone
: 
 - IEnumDot11AdHocNetworks.Next
: 
 - IEnumDot11AdHocNetworks.Reset
: 
 - IEnumDot11AdHocNetworks.Skip
: 
 - IEnumDot11AdHocSecuritySettings.Clone
: 
 - IEnumDot11AdHocSecuritySettings.Next
: 
 - IEnumDot11AdHocSecuritySettings.Reset
: 
 - IEnumDot11AdHocSecuritySettings.Skip
: 
 - IDot11AdHocInterface
: 
 - IDot11AdHocInterfaceNotificationSink
: 
 - IDot11AdHocManager
: 
 - IDot11AdHocManagerNotificationSink
: 
 - IDot11AdHocNetwork
: 
 - IDot11AdHocNetworkNotificationSink
: 
 - IDot11AdHocSecuritySettings
: 
 - IEnumDot11AdHocInterfaces
: 
 - IEnumDot11AdHocNetworks
: 
 - IEnumDot11AdHocSecuritySettings
: 
 - ADsBuildEnumerator
: 
 - ADsBuildVarArrayInt
: 
 - ADsBuildVarArrayStr
: 
 - ADsEncodeBinaryData
: 
 - ADsEnumerateNext
: 
 - ADsFreeEnumerator
: 
 - ADsGetLastError
: 
 - ADsGetObject
: 
 - ADsOpenObject
: 
---

# ADsOpenObject function


## -description


The <b>ADsOpenObject</b> function binds to an ADSI object using explicit user name and password credentials.<b>ADsOpenObject</b> is a wrapper function for <a href="https://msdn.microsoft.com/9daf6f91-6c58-46a8-ba05-149f28b53829">IADsOpenDSObject</a> and is equivalent to the <a href="https://msdn.microsoft.com/9984ddb4-58bb-4264-930b-07e6534dc69f">IADsOpenDSObject::OpenDsObject</a> method.


## -parameters




### -param lpszPathName [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the ADsPath of the ADSI object. For more information and code examples of binding strings for this parameter, see  <a href="https://msdn.microsoft.com/adacf6af-8683-4c3c-91bf-9489f2d5d817">LDAP ADsPath</a> and  <a href="https://msdn.microsoft.com/0fad4b34-5287-43a0-a172-a08955b8b132">WinNT ADsPath</a>.


### -param lpszUserName [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the user name to supply to the directory service to use for credentials. This string should always be in the format "&lt;domain&gt;\&lt;user name&gt;" to avoid ambiguity. For example, if DomainA and DomainB have a trust relationship and both domains have a user with the name "user1", it is not possible to predict which domain <b>ADsOpenObject</b> will use to validate "user1".


### -param lpszPassword [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the password to supply to the directory service to use for credentials.


### -param dwReserved [in]

Type: <b>DWORD</b>

Provider-specific authentication flags used to define the binding options. For more information, see  <a href="https://msdn.microsoft.com/3a45e0c2-5392-456d-80c9-ebd17d056a85">ADS_AUTHENTICATION_ENUM</a>.


### -param riid [in]

Type: <b>REFIID</b>

Interface identifier for the requested interface on this object.


### -param ppObject [out]

Type: <b>VOID**</b>

Pointer to a  pointer to the requested interface.


## -returns



Type: <b>HRESULT</b>

This method supports the standard <b>HRESULT</b> return values, including the following.

For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



This function should not be used just to validate user credentials. For more information about validating user credentials, see Microsoft Knowledge Base article 180548 <a href="http://go.microsoft.com/fwlink/p/?linkid=83979">HOWTO: Validate User Credentials on Microsoft Operating Systems</a>.

A C/C++ client calls the <b>ADsOpenObject</b> helper function to bind to an ADSI object, using the user name and password supplied as credentials for the appropriate directory service. If <i>lpszUsername</i> and <i>lpszPassword</i> are <b>NULL</b> and <b>ADS_SECURE_AUTHENTICATION</b> is set, ADSI binds to the object using the security context of the calling thread, which is either the security context of the user account under which the application is running or of the client user account that the calling thread impersonates.

The  credentials passed to the <b>ADsOpenObject</b> function are used only with the particular object bound to and do not affect the security context of the calling thread. This means that, in the example below, the call to <b>ADsOpenObject</b> will use different credentials than the call to <a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
IADs *padsRoot1;
IADs *padsRoot2;

hr = ADsOpenObject(L"LDAP://rootDSE",
    pwszUsername,
    pwszPassword,
    ADS_SECURE_AUTHENTICATION,
    IID_IADs,
    (LPVOID*)&amp;padsRoot1);

hr = ADsGetObject(L"LDAP://rootDSE",
    IID_IADs,
    (LPVOID*)&amp;padsRoot2);
</pre>
</td>
</tr>
</table></span></div>
To work with the WinNT: provider, you can pass in <i>lpszUsername</i> as one of the following strings:

<ul>
<li>The name of a user account, that is, "jeffsmith".</li>
<li>The Windows style user name, that is, "Fabrikam\jeffsmith".</li>
</ul>
With the LDAP provider for Active Directory, you may pass in <i>lpszUsername</i> as one of the following strings:

<ul>
<li>The name of a user account, such as "jeffsmith". To use a user name by itself, you must set only the <b>ADS_SECURE_AUTHENTICATION</b> flag in the <i>dwReserved</i> parameter.</li>
<li>The user path from a previous version of Windows, such as "Fabrikam\jeffsmith".</li>
<li>Distinguished Name, such as "CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com". To use a DN, the <i>dwReserved</i> parameter must be zero or it must include the <b>ADS_USE_SSL</b> flag.</li>
<li>User Principal Name (UPN), such as "jeffsmith@Fabrikam.com". To use a UPN, assign the appropriate UPN value for the <b>userPrincipalName</b> attribute of the target user object.</li>
</ul>
If Kerberos authentication is required for the successful completion of a specific directory request using the LDAP provider, the <i>lpszPathName</i> binding string must use either a serverless ADsPath, such as "LDAP://CN=Jeff Smith,CN=admin,DC=Fabrikam,DC=com", or it must use an ADsPath with a fully qualified DNS server name, such as "LDAP://central3.corp.Fabrikam.com/CN=Jeff Smith,CN=admin,DC=Fabrikam,DC=com". Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the short name "central3" instead of "central3.corp.Fabrikam.com", may or may not yield Kerberos authentication.

The following code example shows how to bind to a directory service object with the requested user credentials.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pObject;
LPWSTR szUsername = NULL;
LPWSTR szPassword = NULL
HRESULT hr;

// Insert code to securely retrieve the user name and password.

hr = ADsOpenObject(L"LDAP://CN=Jeff,DC=Fabrikam,DC=com",
                   "jeffsmith",
                   "etercespot",
                   ADS_SECURE_AUTHENTICATION, 
                   IID_IADs,
                   (void**) &amp;pObject);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/7b8ded11-e04f-40f5-a82a-5972c4df9dea">ADsOpenObject and IADsOpenDSObject::OpenDsObject</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt270133">Binding</a>



<a href="https://msdn.microsoft.com/9daf6f91-6c58-46a8-ba05-149f28b53829">IADsOpenDSObject</a>



<a href="https://msdn.microsoft.com/9984ddb4-58bb-4264-930b-07e6534dc69f">IADsOpenDSObject::OpenDsObject</a>
 

 

