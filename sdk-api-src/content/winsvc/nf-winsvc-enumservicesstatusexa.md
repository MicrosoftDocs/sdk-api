---
UID: NF:winsvc.EnumServicesStatusExA
title: EnumServicesStatusExA function (winsvc.h)
description: Enumerates services in the specified service control manager database. The name and status of each service are provided, along with additional data based on the specified information level. (ANSI)
helpviewer_keywords: ["EnumServicesStatusExA", "SERVICE_ACTIVE", "SERVICE_DRIVER", "SERVICE_FILE_SYSTEM_DRIVER", "SERVICE_INACTIVE", "SERVICE_KERNEL_DRIVER", "SERVICE_STATE_ALL", "SERVICE_WIN32", "SERVICE_WIN32_OWN_PROCESS", "SERVICE_WIN32_SHARE_PROCESS", "winsvc/EnumServicesStatusExA"]
old-location: base\enumservicesstatusex.htm
tech.root: security
ms.assetid: 7d7940c3-b562-455f-9a21-6d5fb5953030
ms.date: 12/05/2018
ms.keywords: EnumServicesStatusEx, EnumServicesStatusEx function, EnumServicesStatusExA, EnumServicesStatusExW, SERVICE_ACTIVE, SERVICE_DRIVER, SERVICE_FILE_SYSTEM_DRIVER, SERVICE_INACTIVE, SERVICE_KERNEL_DRIVER, SERVICE_STATE_ALL, SERVICE_WIN32, SERVICE_WIN32_OWN_PROCESS, SERVICE_WIN32_SHARE_PROCESS, _win32_enumservicesstatusex, base.enumservicesstatusex, winsvc/EnumServicesStatusEx, winsvc/EnumServicesStatusExA, winsvc/EnumServicesStatusExW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumServicesStatusExW (Unicode) and EnumServicesStatusExA (ANSI)
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
 - EnumServicesStatusExA
 - winsvc/EnumServicesStatusExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Core-l1-1-1.dll
 - AdvApi32Legacy.dll
 - API-Ms-Win-Service-Core-Ansi-L1-1-0.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
 - API-MS-Win-Service-Core-Ansi-L1-1-1.dll
api_name:
 - EnumServicesStatusEx
 - EnumServicesStatusExA
 - EnumServicesStatusExW
---

# EnumServicesStatusExA function


## -description

Enumerates services in the specified service control manager database. The name and status of each service are provided, along with additional data based on the specified information level.

## -parameters

### -param hSCManager [in]

A handle to the service control manager database. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function, and must have the <b>SC_MANAGER_ENUMERATE_SERVICE</b> access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param InfoLevel [in]

The service attributes that are to be returned. Use <b>SC_ENUM_PROCESS_INFO</b> to retrieve the name and service status information for each service in the database. The <i>lpServices</i> parameter is a pointer to a buffer that receives an array of 
<a href="/windows/desktop/api/winsvc/ns-winsvc-enum_service_status_processa">ENUM_SERVICE_STATUS_PROCESS</a> structures. The buffer must be large enough to hold the structures as well as the strings to which their members point.

Currently, no other information levels are defined.

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
Services of type <b>SERVICE_KERNEL_DRIVER</b> and <b>SERVICE_FILE_SYSTEM_DRIVER</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_FILE_SYSTEM_DRIVER"></a><a id="service_file_system_driver"></a><dl>
<dt><b>SERVICE_FILE_SYSTEM_DRIVER</b></dt>
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
<dt>0x00000001</dt>
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
Services of type <b>SERVICE_WIN32_OWN_PROCESS</b> and <b>SERVICE_WIN32_SHARE_PROCESS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32_OWN_PROCESS"></a><a id="service_win32_own_process"></a><dl>
<dt><b>SERVICE_WIN32_OWN_PROCESS</b></dt>
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
Combines the <b>SERVICE_ACTIVE</b> and <b>SERVICE_INACTIVE</b> states.

</td>
</tr>
</table>

### -param lpServices [out, optional]

A pointer to the buffer that receives the status information. The format of this data depends on the value of the <i>InfoLevel</i> parameter.

The maximum size of this array is 256K bytes. To determine the required size, specify <b>NULL</b> for this parameter and 0 for the <i>cbBufSize</i> parameter. The function will fail and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <b>ERROR_MORE_DATA</b>. The <i>pcbBytesNeeded</i> parameter will receive the required size.

<b>Windows Server 2003 and Windows XP:  </b>The maximum size of this array is 64K bytes. This limit was increased as of Windows Server 2003 with SP1 and Windows XP with SP2.

### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpServices</i> parameter, in bytes.

### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to return the remaining service entries, if the buffer is too small.

### -param lpServicesReturned [out]

A pointer to a variable that receives the number of service entries returned.

### -param lpResumeHandle [in, out, optional]

A pointer to a variable that, on input, specifies the starting point of enumeration. You must set this value to zero the first time the 
<b>EnumServicesStatusEx</b> function is called. On output, this value is zero if the function succeeds. However, if the function returns zero and the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_MORE_DATA</b>, this value indicates the next service entry to be read when the 
<b>EnumServicesStatusEx</b> function is called to retrieve the additional data.

### -param pszGroupName [in, optional]

The load-order group name. If this parameter is a string, the only services enumerated are those that belong to the group that has the name specified by the string. If this parameter is an empty string, only services that do not belong to any group are enumerated. If this parameter is <b>NULL</b>, group membership is ignored and all services are enumerated.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following errors may be returned.

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
The handle does not have the <b>SC_MANAGER_ENUMERATE_SERVICE</b> access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small. Not all data in the active database could be returned. The <i>pcbBytesNeeded</i> parameter contains the number of bytes required to receive the remaining entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An illegal parameter value was used.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>InfoLevel</i> parameter contains an unsupported value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHUTDOWN_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The system is shutting down; this function cannot be called.

</td>
</tr>
</table>

## -remarks

If the caller does not have the <b>SERVICE_QUERY_STATUS</b> access right to a service, the service is silently omitted from the list of services returned to the client.





> [!NOTE]
> The winsvc.h header defines EnumServicesStatusEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/ns-winsvc-enum_service_status_processa">ENUM_SERVICE_STATUS_PROCESS</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-installation-removal-and-enumeration">Service Installation, Removal, and Enumeration</a>
