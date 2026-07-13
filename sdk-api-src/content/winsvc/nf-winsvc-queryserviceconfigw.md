---
UID: NF:winsvc.QueryServiceConfigW
title: QueryServiceConfigW function (winsvc.h)
description: Retrieves the configuration parameters of the specified service. (Unicode)
helpviewer_keywords: ["QueryServiceConfig", "QueryServiceConfig function", "QueryServiceConfigW", "_win32_queryserviceconfig", "base.queryserviceconfig", "winsvc/QueryServiceConfig", "winsvc/QueryServiceConfigW"]
old-location: base\queryserviceconfig.htm
tech.root: security
ms.assetid: 364c5f61-dfbe-460b-8e42-5c457b65c050
ms.date: 12/05/2018
ms.keywords: QueryServiceConfig, QueryServiceConfig function, QueryServiceConfigA, QueryServiceConfigW, _win32_queryserviceconfig, base.queryserviceconfig, winsvc/QueryServiceConfig, winsvc/QueryServiceConfigA, winsvc/QueryServiceConfigW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryServiceConfigW (Unicode) and QueryServiceConfigA (ANSI)
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
 - QueryServiceConfigW
 - winsvc/QueryServiceConfigW
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
 - API-MS-Win-Service-management-l2-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - QueryServiceConfig
 - QueryServiceConfigA
 - QueryServiceConfigW
---

# QueryServiceConfigW function


## -description

Retrieves the configuration parameters of the specified service. Optional configuration parameters are available using the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a> function.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function, and it must have the SERVICE_QUERY_CONFIG access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param lpServiceConfig [out, optional]

A pointer to a buffer that receives the service configuration information. The format of the data is a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-query_service_configw">QUERY_SERVICE_CONFIG</a> structure.

The maximum size of this array is 8K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>cbBufSize</i> parameter. The function will fail and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER. The <i>pcbBytesNeeded</i> parameter will receive the required size.

### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpServiceConfig</i> parameter, in bytes.

### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to store all the configuration information, if the function fails with ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
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
The handle does not have the SERVICE_QUERY_CONFIG access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
There is more service configuration information than would fit into the <i>lpServiceConfig</i> buffer. The number of bytes required to get all the information is returned in the <i>pcbBytesNeeded</i> parameter. Nothing is written to <i>lpServiceConfig</i>.

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
</table>

## -remarks

The 
<b>QueryServiceConfig</b> function returns the service configuration information kept in the registry for a particular service. This configuration information is first set by a service control program using the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function. This information may have been updated by a service configuration program using the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a> function.

If the service was running when the configuration information was last changed, the information returned by 
<b>QueryServiceConfig</b> will not reflect the current configuration of the service. Instead, it will reflect the configuration of the service when it is next run. The <b>DisplayName</b> key is an exception to this. When the <b>DisplayName</b> key is changed, it takes effect immediately, regardless of whether the service is running.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/querying-a-service-s-configuration">Querying a Service's Configuration</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines QueryServiceConfig as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-query_service_configa">QUERY_SERVICE_CONFIG</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicedynamicinformation">QueryServiceDynamicInformation</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity">QueryServiceObjectSecurity</a>



<a href="/windows/desktop/Services/service-configuration">Service Configuration</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>
