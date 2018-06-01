---
UID: NF:adshlp.ADsGetLastError
title: ADsGetLastError function
author: windows-sdk-content
description: The ADsGetLastError function retrieves the calling thread's last-error code value.
old-location: adsi\adsgetlasterror.htm
old-project: ADSI
ms.assetid: 5e9899e9-e51e-4785-812a-f86eac6e2006
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ADsGetLastError, ADsGetLastError function [ADSI], _ds_adsgetlasterror, adshlp/ADsGetLastError, adsi.adsgetlasterror
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
-	AdsLdpc.dll
 - accctrl.h
: 
api_name:
-	ADsGetLastError
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
req.dll: Activeds.dll; AdsLdpc.dll
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
---

# ADsGetLastError function


## -description


The <b>ADsGetLastError</b> function retrieves the calling thread's last-error code value.


## -parameters




### -param lpError [out]

Type: <b>LPDWORD</b>

Pointer to the location that receives the error code.


### -param lpErrorBuf [out]

Type: <b>LPWSTR</b>

Pointer to the location that receives the null-terminated Unicode string that describes the error.


### -param dwErrorBufLen [in]

Type: <b>DWORD</b>

Size, in characters, of the <i>lpErrorBuf</i> buffer. If the buffer is too small to receive the error string, the string is truncated, but still null-terminated. A buffer, of at least 256 bytes, is recommended.


### -param lpNameBuf [out]

Type: <b>LPWSTR</b>

Pointer to the location that receives the null-terminated Unicode string that describes the name of the provider that raised the error.


### -param dwNameBufLen [in]

Type: <b>DWORD</b>

Size, in characters, of the <i>lpNameBuf</i> buffer. If the buffer is too small to receive the name of the provider, the string is truncated, but still null-terminated.


## -returns



Type: <b>HRESULT</b>

This method supports standard return values, as well as the following.




## -remarks



ADSI errors fall into two types according to the values of their facility code. The standard ADSI error codes have a facility code value of 0x5 and the extended ADSI error codes assume that of FACILITY_WIN32. The error values of the standard and extended ADSI error codes are of the forms of 0x80005xxx and 0x8007xxxx, respectively. Use the HRESULT_FACILITY(hr) macro to determine the ADSI error type.
   


<div class="alert"><b>Note</b>  The WinNT ADSI provider does not support <b>ADsGetLastError</b>.</div>
<div> </div>
The following code example shows how to get Win32 error codes and their descriptions using <b>ADsGetLastError</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (FAILED(hr))
{
    wprintf(L"An error occurred.\n  HRESULT: %x\n",hr);
    // If facility is Win32, get the Win32 error 
    if (HRESULT_FACILITY(hr)==FACILITY_WIN32)
    {
        DWORD dwLastError;
        WCHAR szErrorBuf[MAX_PATH];
        WCHAR szNameBuf[MAX_PATH];
        // Get extended error value.
        HRESULT hr_return =S_OK;
        hr_return = ADsGetLastError( &amp;dwLastError,
                                       szErrorBuf,
                                       MAX_PATH,
                                       szNameBuf,
                                       MAX_PATH);
        if (SUCCEEDED(hr_return))
        {
             wprintf(L"Error Code: %d\n Error Text: %ws\n Provider: %ws\n", dwLastError, szErrorBuf, szNameBuf);
        }
    }
}</pre>
</td>
</tr>
</table></span></div>
If hr is 80071392, the code example returns the following.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>An error occurred.
    HRESULT: 80071392
    Error Code: 8305
    Error Text: 00002071: UpdErr: DSID-030502F1, problem 6005 (ENTRY_EXISTS), data 0
    Provider: LDAP Provider</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  The WinNT ADSI provider does not support <b>ADsGetLastError</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/c9433af7-2ca5-492a-9b8e-9dfedb5e4d9d">ADsSetLastError</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

