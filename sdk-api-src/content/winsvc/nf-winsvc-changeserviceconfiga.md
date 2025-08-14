---
UID: NF:winsvc.ChangeServiceConfigA
title: ChangeServiceConfigA function (winsvc.h)
description: Changes the configuration parameters of a service. (ANSI)
old-location: base\changeserviceconfig.htm
tech.root: Services
ms.assetid: add8a99b-aced-4341-9790-86efac76df6b
ms.date: 12/05/2018
ms.keywords: ChangeServiceConfig, ChangeServiceConfig function, ChangeServiceConfigA, ChangeServiceConfigW, SERVICE_AUTO_START, SERVICE_BOOT_START, SERVICE_DEMAND_START, SERVICE_DISABLED, SERVICE_ERROR_CRITICAL, SERVICE_ERROR_IGNORE, SERVICE_ERROR_NORMAL, SERVICE_ERROR_SEVERE, SERVICE_FILE_SYSTEM_DRIVER, SERVICE_INTERACTIVE_PROCESS, SERVICE_KERNEL_DRIVER, SERVICE_SYSTEM_START, SERVICE_WIN32_OWN_PROCESS, SERVICE_WIN32_SHARE_PROCESS, _win32_changeserviceconfig, base.changeserviceconfig, winsvc/ChangeServiceConfig, winsvc/ChangeServiceConfigA, winsvc/ChangeServiceConfigW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ChangeServiceConfigW (Unicode) and ChangeServiceConfigA (ANSI)
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
 - ChangeServiceConfigA
 - winsvc/ChangeServiceConfigA
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
 - API-MS-Win-Service-management-l2-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - ChangeServiceConfig
 - ChangeServiceConfigA
 - ChangeServiceConfigW
---

# ChangeServiceConfigA function


## -description

Changes the configuration parameters of a service.

To change the optional configuration parameters, use the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a> function.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function and must have the <b>SERVICE_CHANGE_CONFIG</b> access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param dwServiceType [in]

The type of service. Specify <b>SERVICE_NO_CHANGE</b> if you are not changing the existing service type; otherwise, specify one of the following service types.

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
 

If you specify either <b>SERVICE_WIN32_OWN_PROCESS</b> or <b>SERVICE_WIN32_SHARE_PROCESS</b>, and the service is running in the context of the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>, you can also specify the following type.

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

The service start options. Specify <b>SERVICE_NO_CHANGE</b> if you are not changing the existing start type; otherwise, specify one of the following values.

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

### -param dwErrorControl [in]

The severity of the error, and action taken, if this service fails to start. Specify <b>SERVICE_NO_CHANGE</b> if you are not changing the existing error control; otherwise, specify one of the following values.

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

The fully qualified path to the service binary file. Specify NULL if you are not changing the existing path. If the path contains a space, it must be quoted so that it is correctly interpreted. For example, "d:\\my share\\myservice.exe" should be specified as "\"d:\\my share\\myservice.exe\"". 




The path can also include arguments for an auto-start service. For example, "d:\\myshare\\myservice.exe arg1 arg2". These arguments are passed to the service entry point (typically the <b>main</b> function).

If you specify a path on another computer, the share must be accessible by the computer account of the local computer because this is the security context used in the remote call. However, this requirement allows any potential vulnerabilities in the remote computer to affect the local computer. Therefore, it is best to use a local file.

### -param lpLoadOrderGroup [in, optional]

The  name of the load ordering group of which this service is a member. Specify NULL if you are not changing the existing group. Specify an empty string if the service does not belong to a group. 




The startup program uses load ordering groups to load groups of services in a specified order with respect to the other groups. The list of load ordering groups is contained in the <b>ServiceGroupOrder</b> value of the following registry key:

<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control</b>

### -param lpdwTagId [out, optional]

A pointer to a variable that receives a tag value that is unique in the group specified in the <i>lpLoadOrderGroup</i> parameter. Specify NULL if you are not changing the existing tag. 




You can use a tag for ordering service startup within a load ordering group by specifying a tag order vector in the <b>GroupOrderList</b> value of the following registry key:

<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control</b>

Tags are only evaluated for driver services that have <b>SERVICE_BOOT_START</b> or <b>SERVICE_SYSTEM_START</b> start types.

### -param lpDependencies [in, optional]

A pointer to a double null-terminated array of null-separated names of services or load ordering groups that the system must start before this service can be started. (Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.) Specify NULL if you are not changing the existing dependencies. Specify an empty string if the service has no dependencies. 




You must prefix group names with SC_GROUP_IDENTIFIER so that they can be distinguished from a service name, because services and service groups share the same name space.

### -param lpServiceStartName [in, optional]

The name of the account under which the service should run. Specify <b>NULL</b> if you are not changing the existing account name. If the service type is <b>SERVICE_WIN32_OWN_PROCESS</b>, use an account name in the form <i>DomainName</i>&#92;<i>UserName</i>. The service process will be logged on as this user. If the account belongs to the built-in domain, you can specify .&#92;<i>UserName</i> (note that the corresponding C/C++ string is ".&#92;&#92;<i>UserName</i>"). For more information, see 
<a href="/windows/desktop/Services/service-user-accounts">Service User Accounts</a> and the warning in the Remarks section. 



						

A shared process can run as any user.

If the service type is <b>SERVICE_KERNEL_DRIVER</b> or <b>SERVICE_FILE_SYSTEM_DRIVER</b>, the name is the driver object name that the system uses to load the device driver. Specify <b>NULL</b> if the driver is to use a default object name created by the I/O system.

A service can be configured to use a managed account or a virtual  account. If the service is configured to use a managed service account, the name is the managed service account name. If the service is configured to use a virtual  account, specify the name as NT SERVICE&#92;<i>ServiceName</i>. For more information about managed service accounts and virtual accounts, see the <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)">Service Accounts Step-by-Step Guide</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Managed service accounts and virtual accounts are not supported until Windows 7 and Windows Server 2008 R2.

### -param lpPassword [in, optional]

The password to the account name specified by the <i>lpServiceStartName</i> parameter. Specify <b>NULL</b> if you are not changing the existing password. Specify an empty string if the account has no password or if the service runs in the LocalService, NetworkService, or LocalSystem account. For more information, see 
<a href="/windows/desktop/Services/service-record-list">Service Record List</a>. 




If the account name specified by the  <i>lpServiceStartName</i> parameter is the name of  a managed service account or virtual account name, the <i>lpPassword</i> parameter must be <b>NULL</b>. 

Passwords are ignored for driver services.

### -param lpDisplayName [in, optional]

The display name to be used by applications to identify the service for its users. Specify <b>NULL</b> if you are not changing the existing display name; otherwise, this string has a maximum length of 256 characters. The name is case-preserved in the service control manager. Display name comparisons are always case-insensitive.

This parameter can specify a localized string using the following format:

@[<i>path</i>\]<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. For more information, see <a href="/windows/desktop/api/winreg/nf-winreg-regloadmuistringa">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.

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
The handle does not have the <b>SERVICE_CHANGE_CONFIG</b> access right.

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
The display name already exists in the service controller manager database, either as a service name or as another display name.

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
<dt><b>ERROR_INVALID_SERVICE_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
The account name does not exist, or a service is specified to share the same binary file as an already installed service but with an account name that is not the same as the installed service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_MARKED_FOR_DELETE</b></dt>
</dl>
</td>
<td width="60%">
The service has been marked for deletion.

</td>
</tr>
</table>

## -remarks

The 
<b>ChangeServiceConfig</b> function changes the configuration information for the specified service in the service control manager database. You can obtain the current configuration information by using the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a> function.

If the configuration is changed for a service that is running, with the exception of <i>lpDisplayName</i>, the changes do not take effect until the service is stopped. To update the credentials without having to restart the service, use the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
Setting the <i>lpServiceStartName</i> parameter changes the logon account of the service. This can cause problems. If you have registered a service principal name (SPN), it would now be registered on the wrong account. Similarly, if you have used an ACE to grant access to a service, it would now grant access to the wrong account.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/changing-a-service-configuration">Changing a Service's Configuration</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicedynamicinformation">QueryServiceDynamicInformation</a>



<a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)">Service Accounts Step-by-Step Guide</a>



<a href="/windows/desktop/Services/service-configuration">Service Configuration</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a>
