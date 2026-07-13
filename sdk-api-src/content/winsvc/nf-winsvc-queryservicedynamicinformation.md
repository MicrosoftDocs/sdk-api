---
UID: NF:winsvc.QueryServiceDynamicInformation
title: QueryServiceDynamicInformation function (winsvc.h)
description: Retrieves dynamic information related to the current service start.
helpviewer_keywords: ["QueryServiceDynamicInformation","QueryServiceDynamicInformation function","SERVICE_DYNAMIC_INFORMATION_LEVEL_START_REASON","base.queryservicedynamicinformation","winsvc/QueryServiceDynamicInformation"]
old-location: base\queryservicedynamicinformation.htm
tech.root: security
ms.assetid: 499b63fd-e77b-4b90-9ee7-ff4b7b12c431
ms.date: 12/05/2018
ms.keywords: QueryServiceDynamicInformation, QueryServiceDynamicInformation function, SERVICE_DYNAMIC_INFORMATION_LEVEL_START_REASON, base.queryservicedynamicinformation, winsvc/QueryServiceDynamicInformation
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - QueryServiceDynamicInformation
 - winsvc/QueryServiceDynamicInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-service-core-l1-1-5.dll
 - api-ms-win-service-core-l1-1-4.dll
 - api-ms-win-service-core-l1-1-3.dll
 - Advapi32.dll
 - API-MS-Win-Service-Core-l1-1-1.dll
 - sechost.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
api_name:
 - QueryServiceDynamicInformation
---

# QueryServiceDynamicInformation function


## -description

Retrieves dynamic information related to the current service start.

## -parameters

### -param hServiceStatus [in]

A service status handle provided by <a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>

### -param dwInfoLevel [in]

Indicates the information level.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_DYNAMIC_INFORMATION_LEVEL_START_REASON"></a><a id="service_dynamic_information_level_start_reason"></a><dl>
<dt><b>SERVICE_DYNAMIC_INFORMATION_LEVEL_START_REASON</b></dt>
</dl>
</td>
<td width="60%">
Indicates a request for dynamic information related to the current service start.

</td>
</tr>
</table>

### -param ppDynamicInfo

A dynamic information buffer. If this parameter is valid, the callback function must free the          buffer after use with the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

If the function succeeds, the return value is TRUE.

If the function fails, the return value is FALSE. When this happens the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function should be called to retrieve the error code.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity">QueryServiceObjectSecurity</a>



<a href="/windows/desktop/Services/service-configuration">Service Configuration</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>