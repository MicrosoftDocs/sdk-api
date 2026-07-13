---
UID: NF:winsvc.EnumServicesStatusW
title: EnumServicesStatusW function (winsvc.h)
description: Enumerates services in the specified service control manager database. The name and status of each service are provided. (Unicode)
helpviewer_keywords: ["EnumServicesStatus", "EnumServicesStatus function", "EnumServicesStatusW", "SERVICE_ACTIVE", "SERVICE_DRIVER", "SERVICE_FILE_SYSTEM_DRIVER", "SERVICE_INACTIVE", "SERVICE_KERNEL_DRIVER", "SERVICE_STATE_ALL", "SERVICE_WIN32", "SERVICE_WIN32_OWN_PROCESS", "SERVICE_WIN32_SHARE_PROCESS", "_win32_enumservicesstatus", "base.enumservicesstatus", "winsvc/EnumServicesStatus", "winsvc/EnumServicesStatusW"]
old-location: base\enumservicesstatus.htm
tech.root: security
ms.assetid: 3a82ac0e-f3e8-4a5a-9b13-84e952712229
ms.date: 12/05/2018
ms.keywords: EnumServicesStatus, EnumServicesStatus function, EnumServicesStatusA, EnumServicesStatusW, SERVICE_ACTIVE, SERVICE_DRIVER, SERVICE_FILE_SYSTEM_DRIVER, SERVICE_INACTIVE, SERVICE_KERNEL_DRIVER, SERVICE_STATE_ALL, SERVICE_WIN32, SERVICE_WIN32_OWN_PROCESS, SERVICE_WIN32_SHARE_PROCESS, _win32_enumservicesstatus, base.enumservicesstatus, winsvc/EnumServicesStatus, winsvc/EnumServicesStatusA, winsvc/EnumServicesStatusW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumServicesStatusW (Unicode) and EnumServicesStatusA (ANSI)
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
 - EnumServicesStatusW
 - winsvc/EnumServicesStatusW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-service-legacy-l1-1-0.dll
 - Advapi32.dll
api_name:
 - EnumServicesStatus
 - EnumServicesStatusA
 - EnumServicesStatusW
---

# EnumServicesStatusW function


## -description

Enumerates services in the specified service control manager database. The name and status of each service are provided.

This function has been superseded by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusexa">EnumServicesStatusEx</a> function. It returns the same information 
<b>EnumServicesStatus</b> returns, plus the process identifier and additional information for the service. In addition, 
<b>EnumServicesStatusEx</b> enables you to enumerate services that belong to a specified group.

## -parameters

### -param hSCManager [in]

A handle to the service control manager database. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function, and must have the SC_MANAGER_ENUMERATE_SERVICE access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param dwServiceType [in]

The type of services to be enumerated. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_DRIVER"></a><a id="service_driver"></a><dl>
<dt><b>SERVICE_DRIVER</b></dt>
<dt>0x0000000B</dt>
</dl>
</td>
<td width="60%">
Services of type SERVICE_KERNEL_DRIVER and SERVICE_FILE_SYSTEM_DRIVER.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_FILE_SYSTEM_DRIVER_"></a><a id="service_file_system_driver_"></a><dl>
<dt><b>SERVICE_FILE_SYSTEM_DRIVER </b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
File system driver services.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_KERNEL_DRIVER"></a><a id="service_kernel_driver"></a><dl>
<dt><b>SERVICE_KERNEL_DRIVER</b></dt>
<dt>0x00000001 </dt>
</dl>
</td>
<td width="60%">
Driver services.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32"></a><a id="service_win32"></a><dl>
<dt><b>SERVICE_WIN32</b></dt>
<dt>0x00000030</dt>
</dl>
</td>
<td width="60%">
Services of type SERVICE_WIN32_OWN_PROCESS and SERVICE_WIN32_SHARE_PROCESS.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32_OWN_PROCESS_"></a><a id="service_win32_own_process_"></a><dl>
<dt><b>SERVICE_WIN32_OWN_PROCESS </b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Services that run in their own processes. 

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32_SHARE_PROCESS"></a><a id="service_win32_share_process"></a><dl>
<dt><b>SERVICE_WIN32_SHARE_PROCESS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Services that share a process with one or more other services. For more information, see <a href="/windows/desktop/Services/service-programs">Service Programs</a>.

</td>
</tr>
</table>

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
Enumerates services that are in the following states: SERVICE_START_PENDING, SERVICE_STOP_PENDING, SERVICE_RUNNING, SERVICE_CONTINUE_PENDING, SERVICE_PAUSE_PENDING, and SERVICE_PAUSED.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_INACTIVE"></a><a id="service_inactive"></a><dl>
<dt><b>SERVICE_INACTIVE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enumerates services that are in the SERVICE_STOPPED state.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STATE_ALL"></a><a id="service_state_all"></a><dl>
<dt><b>SERVICE_STATE_ALL</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Combines the following states: SERVICE_ACTIVE and SERVICE_INACTIVE.

</td>
</tr>
</table>

### -param lpServices [out, optional]

A pointer to a buffer that contains an array of 
<a href="/windows/desktop/api/winsvc/ns-winsvc-enum_service_statusa">ENUM_SERVICE_STATUS</a> structures that receive the name and service status information for each service in the database. The buffer must be large enough to hold the structures, plus the strings to which their members point.

The maximum size of this array is 256K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>cbBufSize</i> parameter. The function will fail and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER. The <i>pcbBytesNeeded</i> parameter will receive the required size.

<b>Windows Server 2003 and Windows XP:  </b>The maximum size of this array is 64K bytes. This limit was increased as of Windows Server 2003 with SP1 and Windows XP with SP2.

### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpServices</i> parameter, in bytes.

### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to return the remaining service entries, if the buffer is too small.

### -param lpServicesReturned [out]

A pointer to a variable that receives the number of service entries returned.

### -param lpResumeHandle [in, out, optional]

A pointer to a variable that, on input, specifies the starting point of enumeration. You must set this value to zero the first time this function is called. On output, this value is zero if the function succeeds. However, if the function returns zero and the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns ERROR_MORE_DATA, this value is used to indicate the next service entry to be read when the function is called to retrieve the additional data.

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
The handle does not have the SC_MANAGER_ENUMERATE_SERVICE access right.

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
There are more service entries than would fit into the <i>lpServices</i> buffer. The actual number of service entries written to <i>lpServices</i> is returned in the <i>lpServicesReturned</i> parameter. The number of bytes required to get the remaining entries is returned in the <i>pcbBytesNeeded</i> parameter. The remaining services can be enumerated by additional calls to 
<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusa">EnumServicesStatus</a> with the <i>lpResumeHandle</i> parameter indicating the next service to read.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsvc/ns-winsvc-enum_service_statusa">ENUM_SERVICE_STATUS</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumdependentservicesa">EnumDependentServices</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusexa">EnumServicesStatusEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-installation-removal-and-enumeration">Service Installation, Removal, and Enumeration</a>

## -remarks

> [!NOTE]
> The winsvc.h header defines EnumServicesStatus as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
