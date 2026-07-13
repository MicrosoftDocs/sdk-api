---
UID: NF:winsvc.DeleteService
title: DeleteService function (winsvc.h)
description: Marks the specified service for deletion from the service control manager database.
helpviewer_keywords: ["DeleteService","DeleteService function","_win32_deleteservice","base.deleteservice","winsvc/DeleteService"]
old-location: base\deleteservice.htm
tech.root: security
ms.assetid: 5b0fc714-60e0-4ae3-8fa8-ace36dab2fb0
ms.date: 12/05/2018
ms.keywords: DeleteService, DeleteService function, _win32_deleteservice, base.deleteservice, winsvc/DeleteService
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
 - DeleteService
 - winsvc/DeleteService
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
 - API-MS-Win-Service-management-l1-1-0.dll
api_name:
 - DeleteService
---

# DeleteService function


## -description

Marks the specified service for deletion from the service control manager database.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function, and it must have the DELETE access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes may be set by the service control manager. Others may be set by the registry functions that are called by the service control manager.

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
The handle does not have the DELETE access right.

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
<dt><b>ERROR_SERVICE_MARKED_FOR_DELETE</b></dt>
</dl>
</td>
<td width="60%">
The specified service has already been marked for deletion.

</td>
</tr>
</table>

## -remarks

The 
<b>DeleteService</b> function marks a service for deletion from the service control manager database. The database entry is not removed until all open handles to the service have been closed by calls to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a> function, and the service is not running. A running service is stopped by a call to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a> function with the SERVICE_CONTROL_STOP control code. If the service cannot be stopped, the database entry is removed when the system is restarted.

The service control manager deletes the service by deleting the service key and its subkeys from the registry.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/deleting-a-service">Deleting a Service</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-installation-removal-and-enumeration">Service Installation, Removal, and Enumeration</a>