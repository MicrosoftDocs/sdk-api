---
UID: NF:winsvc.CreateServiceW
title: CreateServiceW function (winsvc.h)
description: Creates a service object and adds it to the specified service control manager database. (Unicode)
old-location: base\createservice.htm
tech.root: Services
ms.assetid: 47288924-3294-4a50-b27d-7df80d5c957c
ms.date: 12/05/2018
ms.keywords: CreateService, CreateService function, CreateServiceA, CreateServiceW, SERVICE_ADAPTER, SERVICE_AUTO_START, SERVICE_BOOT_START, SERVICE_DEMAND_START, SERVICE_DISABLED, SERVICE_ERROR_CRITICAL, SERVICE_ERROR_IGNORE, SERVICE_ERROR_NORMAL, SERVICE_ERROR_SEVERE, SERVICE_FILE_SYSTEM_DRIVER, SERVICE_INTERACTIVE_PROCESS, SERVICE_KERNEL_DRIVER, SERVICE_RECOGNIZER_DRIVER, SERVICE_SYSTEM_START, SERVICE_USER_OWN_PROCESS, SERVICE_WIN32_SHARE_PROCESS, _win32_createservice, base.createservice, winsvc/CreateService, winsvc/CreateServiceA, winsvc/CreateServiceW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateServiceW (Unicode) and CreateServiceA (ANSI)
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
 - CreateServiceW
 - winsvc/CreateServiceW
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
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - CreateService
 - CreateServiceA
 - CreateServiceW
---

# CreateServiceW function


## -description

Creates a service object and adds it to the specified service control manager database.

## -parameters

### -param hSCManager [in]

A handle to the service control manager database. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function and must have the <b>SC_MANAGER_CREATE_SERVICE</b> access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param lpServiceName [in]

The name of the service to install. The maximum string length is 256 characters. The service control manager database preserves the case of the characters, but service name comparisons are always case insensitive. Forward-slash (/) and backslash (\\) are not valid service name characters.

### -param lpDisplayName [in, optional]

The display name to be used by user interface programs to identify the service. This string has a maximum length of 256 characters. The name is case-preserved in the service control manager. Display name comparisons are always case-insensitive.

### -param dwDesiredAccess [in]

The access to the service. Before granting the requested access, the system checks the access token of the calling process. For a list of values, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param dwServiceType [in]

The service type. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ADAPTER"></a><a id="service_adapter"></a><dl>
<dt><b>SERVICE_ADAPTER</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
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
<td width="40%"><a id="SERVICE_RECOGNIZER_DRIVER"></a><a id="service_recognizer_driver"></a><dl>
<dt><b>SERVICE_RECOGNIZER_DRIVER</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Reserved.

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
Service that shares a process with one or more other services. For more information, see <a href="/windows/desktop/Services/service-programs">Service Programs</a>.

</td>
</tr>

</table>
 

If you specify either <b>SERVICE_WIN32_OWN_PROCESS</b> or <b>SERVICE_WIN32_SHARE_PROCESS</b>, and the service is running in the context of the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>, you can also specify the following value.

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

### -param dwStartType [in]

The service start options. This parameter can be one of the following values.

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
A service started automatically by the service control manager during system startup. For more information, see <a href="/windows/desktop/Services/automatically-starting-services">Automatically Starting Services</a>.

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
<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a> function. For more information, see <a href="/windows/desktop/Services/starting-services-on-demand">Starting Services on Demand</a>.

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

### -param dwErrorControl [in]

The severity of the error, and action taken, if this service fails to start. This parameter can be one of the following values.

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
The startup program logs the error in the event log, if possible. If the last-known-good configuration is being started, the startup operation fails. Otherwise, the system is restarted with the last-known good configuration.

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
The startup program logs the error in the event log but continues the startup operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ERROR_SEVERE"></a><a id="service_error_severe"></a><dl>
<dt><b>SERVICE_ERROR_SEVERE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The startup program logs the error in the event log. If the last-known-good configuration is being started, the startup operation continues. Otherwise, the system is restarted with the last-known-good configuration.

</td>
</tr>
</table>

### -param lpBinaryPathName [in, optional]

The fully qualified path to the service binary file. If the path contains a space, it must be quoted so that it is correctly interpreted. For example, "d:\\my share\\myservice.exe" should be specified as "\"d:\\my share\\myservice.exe\"". 




The path can also include arguments for an auto-start service. For example, "d:\\myshare\\myservice.exe arg1 arg2". These arguments are passed to the service entry point (typically the <b>main</b> function).

If you specify a path on another computer, the share must be accessible by the computer account of the local computer because this is the security context used in the remote call. However, this requirement allows any potential vulnerabilities in the remote computer to affect the local computer. Therefore, it is best to use a local file.

### -param lpLoadOrderGroup [in, optional]

The names of the load ordering group of which this service is a member. Specify NULL or an empty string if the service does not belong to a group. 




The startup program uses load ordering groups to load groups of services in a specified order with respect to the other groups. The list of load ordering groups is contained in the following registry value: <b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\ServiceGroupOrder</b>

### -param lpdwTagId [out, optional]

A pointer to a variable that receives a tag value that is unique in the group specified in the <i>lpLoadOrderGroup</i> parameter. Specify NULL if you are not changing the existing tag. 




You can use a tag for ordering service startup within a load ordering group by specifying a tag order vector in the following registry value:<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\GroupOrderList</b>



Tags are only evaluated for driver services that have <b>SERVICE_BOOT_START</b> or <b>SERVICE_SYSTEM_START</b> start types.

### -param lpDependencies [in, optional]

A pointer to a double null-terminated array of null-separated names of services or load ordering groups that the system must start before this service. Specify NULL or an empty string if the service has no dependencies. Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group. 




You must prefix group names with <b>SC_GROUP_IDENTIFIER</b> so that they can be distinguished from a service name, because services and service groups share the same name space.

### -param lpServiceStartName [in, optional]

The name of the account under which the service should run. If the service type is SERVICE_WIN32_OWN_PROCESS, use an account name in the form <i>DomainName</i>&#92;<i>UserName</i>. The service process will be logged on as this user. If the account belongs to the built-in domain, you can specify .&#92;<i>UserName</i>. 




If this parameter is NULL, 
<b>CreateService</b> uses the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>. If the service type specifies <b>SERVICE_INTERACTIVE_PROCESS</b>, the service must run in the LocalSystem account.

If this parameter is NT AUTHORITY\LocalService, 
<b>CreateService</b> uses the 
<a href="/windows/desktop/Services/localservice-account">LocalService account</a>. If the parameter is NT AUTHORITY\NetworkService, 
<b>CreateService</b> uses the 
<a href="/windows/desktop/Services/networkservice-account">NetworkService account</a>.

A shared process can run as any user.

If the service type is <b>SERVICE_KERNEL_DRIVER</b> or <b>SERVICE_FILE_SYSTEM_DRIVER</b>, the name is the driver object name that the system uses to load the device driver. Specify NULL if the driver is to use a default object name created by the I/O system.

A service can be configured to use a managed account or a virtual  account. If the service is configured to use a managed service account, the name is the managed service account name. If the service is configured to use a virtual  account, specify the name as NT SERVICE&#92;<i>ServiceName</i>. For more information about managed service accounts and virtual accounts, see the <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)">Service Accounts Step-by-Step Guide</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Managed service accounts and virtual accounts are not supported until Windows 7 and Windows Server 2008 R2.

### -param lpPassword [in, optional]

The password to the account name specified by the <i>lpServiceStartName</i> parameter. Specify an empty string if the account has no password or if the service runs in the LocalService, NetworkService, or LocalSystem account. For more information, see 
<a href="/windows/desktop/Services/service-record-list">Service Record List</a>. 




If the account name specified by the  <i>lpServiceStartName</i> parameter is the name of  a managed service account or virtual account name, the <i>lpPassword</i> parameter must be NULL. 

Passwords are ignored for driver services.

## -returns

If the function succeeds, the return value is a handle to the service.

If the function fails, the return value is NULL. To get extended error information, call 
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
The handle to the SCM database does not have the <b>SC_MANAGER_CREATE_SERVICE</b> access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CIRCULAR_DEPENDENCY</b></dt>
</dl>
</td>
<td width="60%">
A circular service dependency was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUPLICATE_SERVICE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The display name already exists in the service control manager database either as a service name or as another display name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle to the specified service control manager database is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The specified service name is invalid.

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
<dt><b>ERROR_INVALID_SERVICE_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
The user account name specified in the <i>lpServiceStartName</i> parameter does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified service already exists in this database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_MARKED_FOR_DELETE</b></dt>
</dl>
</td>
<td width="60%">
The specified service already exists in this database and has been marked for deletion.

</td>
</tr>
</table>

## -remarks

The 
<b>CreateService</b> function creates a service object and installs it in the service control manager database by creating a key with the same name as the service under the following registry key:<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services</b>



Information specified by 
<b>CreateService</b>, 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>, and 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a> is saved as values under this key. The following are examples of values stored for a service.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>DependOnGroup</b></td>
<td>Load-ordering groups on which this service depends, as specified by <i>lpDependencies</i>.</td>
</tr>
<tr>
<td><b>DependOnService</b></td>
<td>Services on which this service depends, as specified by <i>lpDependencies</i>.</td>
</tr>
<tr>
<td><b>Description</b></td>
<td>Description specified by 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>.</td>
</tr>
<tr>
<td><b>DisplayName</b></td>
<td>Display name specified by <i>lpDisplayName</i>.</td>
</tr>
<tr>
<td><b>ErrorControl</b></td>
<td>Error control specified by <i>dwErrorControl</i>.</td>
</tr>
<tr>
<td><b>FailureActions</b></td>
<td>Failure actions specified by 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>.</td>
</tr>
<tr>
<td><b>Group</b></td>
<td>Load ordering group specified by <i>lpLoadOrderGroup</i>. Note that setting this value can override the setting of the <b>DependOnService</b> value.</td>
</tr>
<tr>
<td><b>ImagePath</b></td>
<td>Name of binary file, as specified by <i>lpBinaryPathName</i>.</td>
</tr>
<tr>
<td><b>ObjectName</b></td>
<td>Account name specified by <i>lpServiceStartName</i>.</td>
</tr>
<tr>
<td><b>Start</b></td>
<td>When to start service, as specified by <i>dwStartType</i>.</td>
</tr>
<tr>
<td><b>Tag</b></td>
<td>Tag identifier specified by <i>lpdwTagId</i>.</td>
</tr>
<tr>
<td><b>Type</b></td>
<td>Service type specified by <i>dwServiceType</i>.</td>
</tr>
</table>
 

Setup programs and the service itself can create additional subkeys for service-specific information.

The returned handle is only valid for the process that called 
<b>CreateService</b>. It can be closed by calling the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a> function.

If you are creating services that share a process, avoid calling functions with process-wide effects, such as 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a>. In addition, do not unload your service DLL.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/installing-a-service">Installing a Service</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-deleteservice">DeleteService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumdependentservicesa">EnumDependentServices</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicedynamicinformation">QueryServiceDynamicInformation</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity">QueryServiceObjectSecurity</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a>



<a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)">Service Accounts Step-by-Step Guide</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-installation-removal-and-enumeration">Service Installation, Removal, and Enumeration</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity">SetServiceObjectSecurity</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a>
