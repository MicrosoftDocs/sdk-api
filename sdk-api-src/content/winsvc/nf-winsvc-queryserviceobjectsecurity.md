---
UID: NF:winsvc.QueryServiceObjectSecurity
title: QueryServiceObjectSecurity function (winsvc.h)
description: Retrieves a copy of the security descriptor associated with a service object.
helpviewer_keywords: ["QueryServiceObjectSecurity","QueryServiceObjectSecurity function [Security]","_win32_queryserviceobjectsecurity","security.queryserviceobjectsecurity","winsvc/QueryServiceObjectSecurity"]
old-location: security\queryserviceobjectsecurity.htm
tech.root: security
ms.assetid: 5d95945f-f11b-42af-b302-8d924917b9ab
ms.date: 12/05/2018
ms.keywords: QueryServiceObjectSecurity, QueryServiceObjectSecurity function [Security], _win32_queryserviceobjectsecurity, security.queryserviceobjectsecurity, winsvc/QueryServiceObjectSecurity
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
 - QueryServiceObjectSecurity
 - winsvc/QueryServiceObjectSecurity
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
 - QueryServiceObjectSecurity
---

# QueryServiceObjectSecurity function


## -description

The <b>QueryServiceObjectSecurity</b> function retrieves a copy of the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> associated with a service object. You can also use the <a href="/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a> function to retrieve a security descriptor.

## -parameters

### -param hService [in]

A handle to the service control manager or the service. Handles to the service control manager are returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function, and handles to a service are returned by either the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function. The handle must have the READ_CONTROL access right.

### -param dwSecurityInformation [in]

A set of 
bit flags that indicate the type of security information to retrieve. This parameter can be a combination of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags, with the exception that this function does not support the <b>LABEL_SECURITY_INFORMATION</b> value.

### -param lpSecurityDescriptor [out, optional]

A pointer to a buffer that receives a copy of the security descriptor of the specified service object. The calling process must have the appropriate access to view the specified aspects of the  security descriptor of the object. The 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure is returned in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> format.

### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpSecurityDescriptor</i> parameter, in bytes. The largest size allowed is 8 kilobytes.

### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to return the requested security descriptor information, if the function fails.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes may be set by the service control manager. Other error codes may be set by the registry functions that are called by the service control manager.

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
The specified handle was not opened with READ_CONTROL access, or the calling process is not the owner of the object.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor information is too large for the <i>lpSecurityDescriptor</i> buffer. The number of bytes required to get all the information is returned in the <i>pcbBytesNeeded</i> parameter. Nothing is written to the <i>lpSecurityDescriptor</i> buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified security information is not valid.

</td>
</tr>
</table>

## -remarks

When a service is created, the service control manager assigns a default security descriptor to the service object. To retrieve a copy of the security descriptor for a service object, call the <b>QueryServiceObjectSecurity</b> function. To change the security descriptor, call the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity">SetServiceObjectSecurity</a> function. For a description of the default security descriptor for a service object, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

To read the owner, group, or DACL from the security descriptor of the service object, the calling process must have been granted READ_CONTROL access when the handle was opened. To get READ_CONTROL access, the caller must be the owner of the object or the DACL of the object must grant the access.

To read the SACL from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the handle was opened. The correct way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity">SetServiceObjectSecurity</a>