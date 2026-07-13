---
UID: NF:winsvc.OpenServiceA
title: OpenServiceA function (winsvc.h)
description: Opens an existing service. (ANSI)
helpviewer_keywords: ["OpenServiceA", "winsvc/OpenServiceA"]
old-location: base\openservice.htm
tech.root: security
ms.assetid: e0a42613-95ad-4d0f-a464-c6df33014064
ms.date: 12/05/2018
ms.keywords: OpenService, OpenService function, OpenServiceA, OpenServiceW, _win32_openservice, base.openservice, winsvc/OpenService, winsvc/OpenServiceA, winsvc/OpenServiceW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenServiceW (Unicode) and OpenServiceA (ANSI)
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
 - OpenServiceA
 - winsvc/OpenServiceA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Service-management-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - OpenService
 - OpenServiceA
 - OpenServiceW
---

# OpenServiceA function


## -description

Opens an existing service.

## -parameters

### -param hSCManager [in]

A handle to the service control manager database. The 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function returns this handle. For more information, see <a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param lpServiceName [in]

The name of the service to be opened. This is the name specified by the <i>lpServiceName</i> parameter of the <a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function when the service object was created, not the service display name that is shown by user interface applications to identify the service. 

The maximum string length is 256 characters. The service control manager database preserves the case of the characters, but service name comparisons are always case insensitive. Forward-slash (/) and backslash (\\) are invalid service name characters.

### -param dwDesiredAccess [in]

The access to the service. For a list of access rights, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>. 




Before granting the requested access, the system checks the access token of the calling process against the discretionary access-control list of the security descriptor associated with the service object.

## -returns

If the function succeeds, the return value is a handle to the service.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes can be set by the service control manager. Others can be set by the registry functions that are called by the service control manager.

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
The handle does not have access to the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The specified service name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified service does not exist.

</td>
</tr>
</table>

## -remarks

The returned handle is only valid for the process that called 
<b>OpenService</b>. It can be closed by calling the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a> function.

To use <b>OpenService</b>, no privileges are required aside from <b>SC_MANAGER_CONNECT</b>.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/starting-a-service">Starting a Service</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines OpenService as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-deleteservice">DeleteService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumdependentservicesa">EnumDependentServices</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicedynamicinformation">QueryServiceDynamicInformation</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity">QueryServiceObjectSecurity</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a>



<a href="/windows/desktop/Services/scm-handles">SCM Handles</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity">SetServiceObjectSecurity</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a>
