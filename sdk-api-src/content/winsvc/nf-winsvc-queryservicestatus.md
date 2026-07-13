---
UID: NF:winsvc.QueryServiceStatus
title: QueryServiceStatus function (winsvc.h)
description: Retrieves the current status of the specified service.
helpviewer_keywords: ["QueryServiceStatus","QueryServiceStatus function","_win32_queryservicestatus","base.queryservicestatus","winsvc/QueryServiceStatus"]
old-location: base\queryservicestatus.htm
tech.root: security
ms.assetid: dcd2d8a1-10ef-4229-b873-b4fc3ec9293f
ms.date: 12/05/2018
ms.keywords: QueryServiceStatus, QueryServiceStatus function, _win32_queryservicestatus, base.queryservicestatus, winsvc/QueryServiceStatus
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
 - QueryServiceStatus
 - winsvc/QueryServiceStatus
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
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - QueryServiceStatus
---

# QueryServiceStatus function


## -description

Retrieves the current status of the specified service.

This function has been superseded by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a> function. 
<b>QueryServiceStatusEx</b> returns the same information 
<b>QueryServiceStatus</b> returns, with the addition of the process identifier and additional information for the service.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function, and it must have the SERVICE_QUERY_STATUS access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param lpServiceStatus [out]

A pointer to a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a> structure that receives the status information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
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
The handle does not have the SERVICE_QUERY_STATUS access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>

## -remarks

The 
<b>QueryServiceStatus</b> function returns the most recent service status information reported to the service control manager. If the service just changed its status, it may not have updated the service control manager yet.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-startup">Service Startup</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>