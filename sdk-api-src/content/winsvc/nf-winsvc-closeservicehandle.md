---
UID: NF:winsvc.CloseServiceHandle
title: CloseServiceHandle function (winsvc.h)
description: Closes a handle to a service control manager or service object.
helpviewer_keywords: ["CloseServiceHandle","CloseServiceHandle function","_win32_closeservicehandle","base.closeservicehandle","winsvc/CloseServiceHandle"]
old-location: base\closeservicehandle.htm
tech.root: security
ms.assetid: 6cf25994-4939-4aff-af38-5ffc8fc606ae
ms.date: 12/05/2018
ms.keywords: CloseServiceHandle, CloseServiceHandle function, _win32_closeservicehandle, base.closeservicehandle, winsvc/CloseServiceHandle
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
 - CloseServiceHandle
 - winsvc/CloseServiceHandle
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
api_name:
 - CloseServiceHandle
---

# CloseServiceHandle function


## -description

Closes a handle to a service control manager or service object.

## -parameters

### -param hSCObject [in]

A handle to the service control manager object or the service object to close. Handles to service control manager objects are returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function, and handles to service objects are returned by either the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error code can be set by the service control manager. Other error codes can be set by registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
</table>

## -remarks

The 
<b>CloseServiceHandle</b> function does not destroy the service control manager object referred to by the handle. A service control manager object cannot be destroyed. A service object can be destroyed by calling the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-deleteservice">DeleteService</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/deleting-a-service">Deleting a Service</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-deleteservice">DeleteService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/Services/scm-handles">SCM Handles</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>