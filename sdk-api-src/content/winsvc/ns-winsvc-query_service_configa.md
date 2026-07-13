---
UID: NS:winsvc._QUERY_SERVICE_CONFIGA
title: QUERY_SERVICE_CONFIGA (winsvc.h)
description: Contains configuration information for an installed service. It is used by the QueryServiceConfig function. (ANSI)
helpviewer_keywords: ["*LPQUERY_SERVICE_CONFIGA","LPQUERY_SERVICE_CONFIG","LPQUERY_SERVICE_CONFIG structure pointer","QUERY_SERVICE_CONFIG","QUERY_SERVICE_CONFIG structure","QUERY_SERVICE_CONFIGA","QUERY_SERVICE_CONFIGW","SERVICE_AUTO_START","SERVICE_BOOT_START","SERVICE_DEMAND_START","SERVICE_DISABLED","SERVICE_ERROR_CRITICAL","SERVICE_ERROR_IGNORE","SERVICE_ERROR_NORMAL","SERVICE_ERROR_SEVERE","SERVICE_FILE_SYSTEM_DRIVER","SERVICE_INTERACTIVE_PROCESS","SERVICE_KERNEL_DRIVER","SERVICE_SYSTEM_START","SERVICE_WIN32_OWN_PROCESS","SERVICE_WIN32_SHARE_PROCESS","_win32_query_service_config_str","base.query_service_config_str","winsvc/LPQUERY_SERVICE_CONFIG","winsvc/QUERY_SERVICE_CONFIG","winsvc/QUERY_SERVICE_CONFIGA","winsvc/QUERY_SERVICE_CONFIGW"]
old-location: base\query_service_config_str.htm
tech.root: security
ms.assetid: 069c1431-a04b-4e96-953b-14c5c0700857
ms.date: 12/05/2018
ms.keywords: '*LPQUERY_SERVICE_CONFIGA, LPQUERY_SERVICE_CONFIG, LPQUERY_SERVICE_CONFIG structure pointer, QUERY_SERVICE_CONFIG, QUERY_SERVICE_CONFIG structure, QUERY_SERVICE_CONFIGA, QUERY_SERVICE_CONFIGW, SERVICE_AUTO_START, SERVICE_BOOT_START, SERVICE_DEMAND_START, SERVICE_DISABLED, SERVICE_ERROR_CRITICAL, SERVICE_ERROR_IGNORE, SERVICE_ERROR_NORMAL, SERVICE_ERROR_SEVERE, SERVICE_FILE_SYSTEM_DRIVER, SERVICE_INTERACTIVE_PROCESS, SERVICE_KERNEL_DRIVER, SERVICE_SYSTEM_START, SERVICE_WIN32_OWN_PROCESS, SERVICE_WIN32_SHARE_PROCESS, _win32_query_service_config_str, base.query_service_config_str, winsvc/LPQUERY_SERVICE_CONFIG, winsvc/QUERY_SERVICE_CONFIG, winsvc/QUERY_SERVICE_CONFIGA, winsvc/QUERY_SERVICE_CONFIGW'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QUERY_SERVICE_CONFIGW (Unicode) and QUERY_SERVICE_CONFIGA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: QUERY_SERVICE_CONFIGA, *LPQUERY_SERVICE_CONFIGA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QUERY_SERVICE_CONFIGA
 - winsvc/_QUERY_SERVICE_CONFIGA
 - LPQUERY_SERVICE_CONFIGA
 - winsvc/LPQUERY_SERVICE_CONFIGA
 - QUERY_SERVICE_CONFIGA
 - winsvc/QUERY_SERVICE_CONFIGA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - QUERY_SERVICE_CONFIG
 - QUERY_SERVICE_CONFIGA
 - QUERY_SERVICE_CONFIGW
---

# QUERY_SERVICE_CONFIGA structure


## -description

Contains configuration information for an installed service. It is used by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a> function.

## -struct-fields

### -field dwServiceType

The type of service. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_FILE_SYSTEM_DRIVER"></a><a id="service_file_system_driver"></a><dl>
<dt><b>SERVICE_FILE_SYSTEM_DRIVER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
File system driver service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_KERNEL_DRIVER"></a><a id="service_kernel_driver"></a><dl>
<dt><b>SERVICE_KERNEL_DRIVER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Driver service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32_OWN_PROCESS"></a><a id="service_win32_own_process"></a><dl>
<dt><b>SERVICE_WIN32_OWN_PROCESS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Service that runs in its own process.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32_SHARE_PROCESS"></a><a id="service_win32_share_process"></a><dl>
<dt><b>SERVICE_WIN32_SHARE_PROCESS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Service that shares a process with other services.

</td>
</tr>
</table>
 

If the value is <b>SERVICE_WIN32_OWN_PROCESS</b> or <b>SERVICE_WIN32_SHARE_PROCESS</b>, and the service is running in the context of the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>, the following type may also be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_INTERACTIVE_PROCESS"></a><a id="service_interactive_process"></a><dl>
<dt><b>SERVICE_INTERACTIVE_PROCESS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The service can interact with the desktop. 




For more information, see 
<a href="/windows/desktop/Services/interactive-services">Interactive Services</a>.

</td>
</tr>
</table>

### -field dwStartType

When to start the service. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_AUTO_START"></a><a id="service_auto_start"></a><dl>
<dt><b>SERVICE_AUTO_START</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
A service started automatically by the service control manager during system startup.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_BOOT_START"></a><a id="service_boot_start"></a><dl>
<dt><b>SERVICE_BOOT_START</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
A device driver started by the system loader. This value is valid only for driver services.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_DEMAND_START"></a><a id="service_demand_start"></a><dl>
<dt><b>SERVICE_DEMAND_START</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
A service started by the service control manager when a process calls the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_DISABLED"></a><a id="service_disabled"></a><dl>
<dt><b>SERVICE_DISABLED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
A service that cannot be started. Attempts to start the service result in the error code <b>ERROR_SERVICE_DISABLED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_SYSTEM_START"></a><a id="service_system_start"></a><dl>
<dt><b>SERVICE_SYSTEM_START</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
A device driver started by the <b>IoInitSystem</b> function. This value is valid only for driver services.

</td>
</tr>
</table>

### -field dwErrorControl

The severity of the error, and action taken, if this service fails to start. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ERROR_CRITICAL"></a><a id="service_error_critical"></a><dl>
<dt><b>SERVICE_ERROR_CRITICAL</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The startup program logs the error in the event log, if possible. If the last-known good configuration is being started, the startup operation fails. Otherwise, the system is restarted with the last-known good configuration.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ERROR_IGNORE"></a><a id="service_error_ignore"></a><dl>
<dt><b>SERVICE_ERROR_IGNORE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The startup program ignores the error and continues the startup operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ERROR_NORMAL"></a><a id="service_error_normal"></a><dl>
<dt><b>SERVICE_ERROR_NORMAL</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The startup program logs the error in the event log and continues the startup operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ERROR_SEVERE"></a><a id="service_error_severe"></a><dl>
<dt><b>SERVICE_ERROR_SEVERE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The startup program logs the error in the event log. If the last-known good configuration is being started, the startup operation continues. Otherwise, the system is restarted with the last-known-good configuration.

</td>
</tr>
</table>

### -field lpBinaryPathName

The fully qualified path to the service binary file. 




The path can also include arguments for an auto-start service. These arguments are passed to the service entry point (typically the <b>main</b> function).

### -field lpLoadOrderGroup

The name of the load ordering group to which this service belongs. If the member is NULL or an empty string, the service does not belong to a load ordering group. 




The startup program uses load ordering groups to load groups of services in a specified order with respect to the other groups. The list of load ordering groups is contained in the following registry value:


<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\ServiceGroupOrder</b>

### -field dwTagId

A unique tag value for this service in the group specified by the <i>lpLoadOrderGroup</i> parameter. A value of zero indicates that the service has not been assigned a tag. You can use a tag for ordering service startup within a load order group by specifying a tag order vector in the registry located at: 


<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\GroupOrderList</b>



Tags are only evaluated for <b>SERVICE_KERNEL_DRIVER</b> and <b>SERVICE_FILE_SYSTEM_DRIVER</b> type services that have <b>SERVICE_BOOT_START</b> or <b>SERVICE_SYSTEM_START</b> start types.

### -field lpDependencies

A pointer to an array of null-separated names of services or load ordering groups that must start before this service. The array is doubly null-terminated. If the pointer is <b>NULL</b> or if it points to an empty string, the service has no dependencies. If a group name is specified, it must be prefixed by the <b>SC_GROUP_IDENTIFIER</b> (defined in WinSvc.h) character to differentiate it from a service name, because services and service groups share the same name space. Dependency on a service means that this service can only run if the service it depends on is running. Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.

### -field lpServiceStartName

If the service type is <b>SERVICE_WIN32_OWN_PROCESS</b> or <b>SERVICE_WIN32_SHARE_PROCESS</b>, this member is the name of the account that the service process will be logged on as when it runs. This name can be of the form <i>Domain</i><b>\\</b><i>UserName</i>. If the account belongs to the built-in domain, the name can be of the form <b>.\\</b><i>UserName</i>. The name can also be "LocalSystem" if the process is running under the LocalSystem account.   



						

If the service type is <b>SERVICE_KERNEL_DRIVER</b> or <b>SERVICE_FILE_SYSTEM_DRIVER</b>, this member is the driver object name (that is, \FileSystem\Rdr or \Driver\Xns) which the input and output (I/O) system uses to load the device driver. If this member is NULL, the driver is to be run with a default object name created by the I/O system, based on the service name.

### -field lpDisplayName

The display name to be used by service control programs to identify the service. This string has a maximum length of 256 characters. The name is case-preserved in the service control manager. Display name comparisons are always case-insensitive.

This parameter can specify a localized string using the following format:

@[<i>Path</i>\]<i>DLLName</i>,-<i>StrID</i>

The string with identifier <i>StrID</i> is loaded from <i>DLLName</i>; the <i>Path</i> is optional. For more information, see <a href="/windows/desktop/api/winreg/nf-winreg-regloadmuistringa">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.

## -remarks

The configuration information for a service is initially specified when the service is created by a call to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function. The information can be modified by calling the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/querying-a-service-s-configuration">Querying a Service's Configuration</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines QUERY_SERVICE_CONFIG as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a>
