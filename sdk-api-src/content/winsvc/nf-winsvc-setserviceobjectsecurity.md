---
UID: NF:winsvc.SetServiceObjectSecurity
title: SetServiceObjectSecurity function
author: windows-sdk-content
description: Sets the security descriptor of a service object.
old-location: security\setserviceobjectsecurity.htm
old-project: SecAuthZ
ms.assetid: 39481d9a-79d5-4bbf-8480-4095a34dddb6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, SetServiceObjectSecurity, SetServiceObjectSecurity function [Security], _win32_setserviceobjectsecurity, security.setserviceobjectsecurity, winsvc/SetServiceObjectSecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-management-l2-1-0.dll
api_name:
 - SetServiceObjectSecurity
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetServiceObjectSecurity function


## -description


<p class="CCE_Message">[<b>SetServiceObjectSecurity</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a> function.]

The <b>SetServiceObjectSecurity</b> function sets the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of a service object.


## -parameters




### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function. The access required for this handle depends on the security information specified in the <i>dwSecurityInformation</i> parameter.


### -param dwSecurityInformation [in]

Specifies the components of the security descriptor to set. This parameter can be a combination of the following values. Note that flags not handled by <b>SetServiceObjectSecurity</b> will be silently ignored. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DACL_SECURITY_INFORMATION"></a><a id="dacl_security_information"></a><dl>
<dt><b>DACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) of the object. The handle specified by <i>hService</i>  must have WRITE_DAC access, or the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must be the owner of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the primary group <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the object. The handle specified by <i>hService</i> must have WRITE_OWNER access, or the calling process must be the owner of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="OWNER_SECURITY_INFORMATION"></a><a id="owner_security_information"></a><dl>
<dt><b>OWNER_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the SID of the owner of the object. The handle specified by <i>hService</i> must have WRITE_OWNER access, or the calling process must be the owner of the object or have the SE_TAKE_OWNERSHIP_NAME privilege enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SACL_SECURITY_INFORMATION"></a><a id="sacl_security_information"></a><dl>
<dt><b>SACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of the object. The handle specified by <i>hService</i> must have ACCESS_SYSTEM_SECURITY access. 

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To obtain ACCESS_SYSTEM_SECURITY access</b>

<ol>
<li>Enable the SE_SECURITY_NAME 
<a href="https://msdn.microsoft.com/fe6aae0f-93eb-4aba-a6ac-45e71c251c51">privilege</a> in the current <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> of the caller.</li>
<li>Open the handle for ACCESS_SYSTEM_SECURITY access.</li>
<li>Disable the privilege.</li>
</ol>
</td>
</tr>
</table>
 


### -param lpSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that contains the new security information.


## -returns



If the function succeeds, the function returns nonzero. 

If the function fails, it  returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The specified handle was not opened with the required access, or the calling process is not the owner of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified security information or security descriptor is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_MARKED_FOR_DELETE</b></dt>
</dl>
</td>
<td width="60%">
The specified service has been marked for deletion.

</td>
</tr>
</table>
 




## -remarks



The <b>SetServiceObjectSecurity</b> function sets the specified portions of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of the service object based on the information specified in the <i>lpSecurityDescriptor</i> buffer. This function replaces any or all of the security information associated with the service object, according to the flags set in the <i>dwSecurityInformation</i> parameter and subject to the access rights of the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>.

When a service is created, the service control manager assigns a default security descriptor to the service object. To retrieve a copy of the security descriptor for a service object, call the 
<a href="https://msdn.microsoft.com/5d95945f-f11b-42af-b302-8d924917b9ab">QueryServiceObjectSecurity</a> function. For a description of the default security descriptor for a service object, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>. 

Note that granting certain access to untrusted users (such as SERVICE_CHANGE_CONFIG or SERVICE_STOP) can allow them to interfere with the execution of your service and possibly allow them to run applications under the LocalSystem account.




## -see-also




<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/5d95945f-f11b-42af-b302-8d924917b9ab">QueryServiceObjectSecurity</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>
 

 

