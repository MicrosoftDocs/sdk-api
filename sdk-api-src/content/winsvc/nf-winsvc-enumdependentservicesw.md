---
UID: NF:winsvc.EnumDependentServicesW
title: EnumDependentServicesW function (winsvc.h)
description: Retrieves the name and status of each service that depends on the specified service. (Unicode)
helpviewer_keywords: ["EnumDependentServices", "EnumDependentServices function", "EnumDependentServicesW", "SERVICE_ACTIVE", "SERVICE_INACTIVE", "SERVICE_STATE_ALL", "_win32_enumdependentservices", "base.enumdependentservices", "winsvc/EnumDependentServices", "winsvc/EnumDependentServicesW"]
old-location: base\enumdependentservices.htm
tech.root: security
ms.assetid: 905d4453-96d4-4055-8a17-36714c547cdd
ms.date: 12/05/2018
ms.keywords: EnumDependentServices, EnumDependentServices function, EnumDependentServicesA, EnumDependentServicesW, SERVICE_ACTIVE, SERVICE_INACTIVE, SERVICE_STATE_ALL, _win32_enumdependentservices, base.enumdependentservices, winsvc/EnumDependentServices, winsvc/EnumDependentServicesA, winsvc/EnumDependentServicesW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDependentServicesW (Unicode) and EnumDependentServicesA (ANSI)
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
 - EnumDependentServicesW
 - winsvc/EnumDependentServicesW
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
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Core-l1-1-1.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
 - AdvApi32Legacy.dll
 - API-MS-Win-Service-Core-Ansi-L1-1-1.dll
api_name:
 - EnumDependentServices
 - EnumDependentServicesA
 - EnumDependentServicesW
---

# EnumDependentServicesW function


## -description

Retrieves the name and status of each service that depends on the specified service; that is, the specified service must be running before the dependent services can run.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function, and it must have the <b>SERVICE_ENUMERATE_DEPENDENTS</b> access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param dwServiceState [in]

The state of the services to be enumerated. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACTIVE"></a><a id="service_active"></a><dl>
<dt><b>SERVICE_ACTIVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enumerates services that are in the following states: <b>SERVICE_START_PENDING</b>, <b>SERVICE_STOP_PENDING</b>, <b>SERVICE_RUNNING</b>, <b>SERVICE_CONTINUE_PENDING</b>, <b>SERVICE_PAUSE_PENDING</b>, and <b>SERVICE_PAUSED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_INACTIVE"></a><a id="service_inactive"></a><dl>
<dt><b>SERVICE_INACTIVE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enumerates services that are in the <b>SERVICE_STOPPED</b> state.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STATE_ALL"></a><a id="service_state_all"></a><dl>
<dt><b>SERVICE_STATE_ALL</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Combines the following states: <b>SERVICE_ACTIVE</b> and <b>SERVICE_INACTIVE</b>.

</td>
</tr>
</table>

### -param lpServices [out, optional]

A pointer to an array of 
<a href="/windows/desktop/api/winsvc/ns-winsvc-enum_service_statusa">ENUM_SERVICE_STATUS</a> structures that receives the name and service status information for each dependent service in the database. The buffer must be large enough to hold the structures, plus the strings to which their members point.

The order of the services in this array is the reverse of the start order of the services. In other words, the first service in the array is the one that would be started last, and the last service in the array is the one that would be started first.

The maximum size of this array is 64,000 bytes. To determine the required size, specify <b>NULL</b> for this parameter and 0 for the <i>cbBufSize</i> parameter. The function will fail and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <b>ERROR_MORE_DATA</b>. The <i>pcbBytesNeeded</i> parameter will receive the required size.

### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpServices</i> parameter, in bytes.

### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to store the array of service entries. The variable only receives this value if the buffer pointed to by <i>lpServices</i> is too small, indicated by function failure and the <b>ERROR_MORE_DATA</b> error; otherwise, the contents of <i>pcbBytesNeeded</i> are undefined.

### -param lpServicesReturned [out]

A pointer to a variable that receives the number of service entries returned.

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
The handle does not have the <b>SERVICE_ENUMERATE_DEPENDENTS</b> access right.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter that was specified is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpServices</i> is not large enough. The function sets the variable pointed to by <i>lpServicesReturned</i> to the actual number of service entries stored into the buffer. The function sets the variable pointed to by <i>pcbBytesNeeded</i> to the number of bytes required to store all of the service entries.

</td>
</tr>
</table>

## -remarks

The returned services entries are ordered in the reverse order of the start order, with group order taken into account. If you need to stop the dependent services, you can use the order of entries written to the <i>lpServices</i> buffer to stop the dependent services in the proper order.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/stopping-a-service">Stopping a Service</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines EnumDependentServices as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-enum_service_statusa">ENUM_SERVICE_STATUS</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusexa">EnumServicesStatusEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-installation-removal-and-enumeration">Service Installation, Removal, and Enumeration</a>
