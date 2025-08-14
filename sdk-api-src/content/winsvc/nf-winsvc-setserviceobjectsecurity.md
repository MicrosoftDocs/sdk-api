---
UID: NF:winsvc.SetServiceObjectSecurity
title: SetServiceObjectSecurity function (winsvc.h)
description: Sets the security descriptor of a service object.
helpviewer_keywords: ["DACL_SECURITY_INFORMATION","GROUP_SECURITY_INFORMATION","OWNER_SECURITY_INFORMATION","SACL_SECURITY_INFORMATION","SetServiceObjectSecurity","SetServiceObjectSecurity function [Security]","_win32_setserviceobjectsecurity","security.setserviceobjectsecurity","winsvc/SetServiceObjectSecurity"]
old-location: security\setserviceobjectsecurity.htm
tech.root: security
ms.assetid: 39481d9a-79d5-4bbf-8480-4095a34dddb6
ms.date: 12/05/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, SetServiceObjectSecurity, SetServiceObjectSecurity function [Security], _win32_setserviceobjectsecurity, security.setserviceobjectsecurity, winsvc/SetServiceObjectSecurity
req.header: winsvc.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetServiceObjectSecurity
 - winsvc/SetServiceObjectSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-management-l2-1-0.dll
api_name:
 - SetServiceObjectSecurity
---

# SetServiceObjectSecurity function


## -description

<p class="CCE_Message">[<b>SetServiceObjectSecurity</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a> function.]

The <b>SetServiceObjectSecurity</b> function sets the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> of a service object.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function. The access required for this handle depends on the security information specified in the <i>dwSecurityInformation</i> parameter.

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
Sets the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) of the object. The handle specified by <i>hService</i>  must have WRITE_DAC access, or the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must be the owner of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the primary group <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the object. The handle specified by <i>hService</i> must have WRITE_OWNER access, or the calling process must be the owner of the object.

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
Sets the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) of the object. The handle specified by <i>hService</i> must have ACCESS_SYSTEM_SECURITY access. 

<p class="proch"><b>To obtain ACCESS_SYSTEM_SECURITY access</b>

<ol>
<li>Enable the SE_SECURITY_NAME 
<a href="/windows/desktop/SecAuthZ/privileges">privilege</a> in the current <a href="/windows/desktop/SecGloss/a-gly">access token</a> of the caller.</li>
<li>Open the handle for ACCESS_SYSTEM_SECURITY access.</li>
<li>Disable the privilege.</li>
</ol>
</td>
</tr>
</table>

### -param lpSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the new security information.

## -returns

If the function succeeds, the function returns nonzero. 

If the function fails, it  returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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

The <b>SetServiceObjectSecurity</b> function sets the specified portions of the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> of the service object based on the information specified in the <i>lpSecurityDescriptor</i> buffer. This function replaces any or all of the security information associated with the service object, according to the flags set in the <i>dwSecurityInformation</i> parameter and subject to the access rights of the calling <a href="/windows/desktop/SecGloss/p-gly">process</a>.

When a service is created, the service control manager assigns a default security descriptor to the service object. To retrieve a copy of the security descriptor for a service object, call the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity">QueryServiceObjectSecurity</a> function. For a description of the default security descriptor for a service object, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>. 

Note that granting certain access to untrusted users (such as SERVICE_CHANGE_CONFIG or SERVICE_STOP) can allow them to interfere with the execution of your service and possibly allow them to run applications under the LocalSystem account.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity">QueryServiceObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>