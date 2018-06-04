---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _QUERY_SERVICE_CONFIGW structure


## -description


Contains configuration information for an installed service. It is used by the 
<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a> function.


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
<a href="https://msdn.microsoft.com/692bceb6-f5bd-4b83-ab3b-ef8099dc84e1">LocalSystem account</a>, the following type may also be specified.

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
<a href="https://msdn.microsoft.com/3d6e090a-00b1-47d8-a4fb-620f3db8ba9c">Interactive Services</a>.

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
<a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a> function.

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

If the service type is <b>SERVICE_WIN32_OWN_PROCESS</b> or <b>SERVICE_WIN32_SHARE_PROCESS</b>, this member is the name of the account that the service process will be logged on as when it runs. This name can be of the form <i>Domain</i><b>\</b><i>UserName</i>. If the account belongs to the built-in domain, the name can be of the form <b>.\</b><i>UserName</i>. The name can also be "LocalSystem" if the process is running under the LocalSystem account.   



						

If the service type is <b>SERVICE_KERNEL_DRIVER</b> or <b>SERVICE_FILE_SYSTEM_DRIVER</b>, this member is the driver object name (that is, \FileSystem\Rdr or \Driver\Xns) which the input and output (I/O) system uses to load the device driver. If this member is NULL, the driver is to be run with a default object name created by the I/O system, based on the service name.


### -field lpDisplayName

The display name to be used by service control programs to identify the service. This string has a maximum length of 256 characters. The name is case-preserved in the service control manager. Display name comparisons are always case-insensitive.

This parameter can specify a localized string using the following format:

@[<i>Path</i>\]<i>DLLName</i>,-<i>StrID</i>

The string with identifier <i>StrID</i> is loaded from <i>DLLName</i>; the <i>Path</i> is optional. For more information, see <a href="https://msdn.microsoft.com/76ffc77f-a1bc-4e01-858f-4a76563a2bbc">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.


## -remarks



The configuration information for a service is initially specified when the service is created by a call to the 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function. The information can be modified by calling the 
<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/e6633dc9-c9b6-457d-8adc-e751ec9cf71d">Querying a Service's Configuration</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a>



<a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a>
 

 

