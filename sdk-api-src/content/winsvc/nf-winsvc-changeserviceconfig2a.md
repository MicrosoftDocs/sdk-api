---
UID: NF:winsvc.ChangeServiceConfig2A
title: ChangeServiceConfig2A function (winsvc.h)
description: Changes the optional configuration parameters of a service. (ANSI)
helpviewer_keywords: ["ChangeServiceConfig2A", "SERVICE_CONFIG_DELAYED_AUTO_START_INFO", "SERVICE_CONFIG_DESCRIPTION", "SERVICE_CONFIG_FAILURE_ACTIONS", "SERVICE_CONFIG_FAILURE_ACTIONS_FLAG", "SERVICE_CONFIG_LAUNCH_PROTECTED", "SERVICE_CONFIG_PREFERRED_NODE", "SERVICE_CONFIG_PRESHUTDOWN_INFO", "SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO", "SERVICE_CONFIG_SERVICE_SID_INFO", "SERVICE_CONFIG_TRIGGER_INFO", "winsvc/ChangeServiceConfig2A"]
old-location: base\changeserviceconfig2.htm
tech.root: security
ms.assetid: 6e5b79ed-52e1-460e-b076-01afbd08775c
ms.date: 12/05/2018
ms.keywords: ChangeServiceConfig2, ChangeServiceConfig2 function, ChangeServiceConfig2A, ChangeServiceConfig2W, SERVICE_CONFIG_DELAYED_AUTO_START_INFO, SERVICE_CONFIG_DESCRIPTION, SERVICE_CONFIG_FAILURE_ACTIONS, SERVICE_CONFIG_FAILURE_ACTIONS_FLAG, SERVICE_CONFIG_LAUNCH_PROTECTED, SERVICE_CONFIG_PREFERRED_NODE, SERVICE_CONFIG_PRESHUTDOWN_INFO, SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO, SERVICE_CONFIG_SERVICE_SID_INFO, SERVICE_CONFIG_TRIGGER_INFO, _win32_changeserviceconfig2, base.changeserviceconfig2, winsvc/ChangeServiceConfig2, winsvc/ChangeServiceConfig2A, winsvc/ChangeServiceConfig2W
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ChangeServiceConfig2W (Unicode) and ChangeServiceConfig2A (ANSI)
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
 - ChangeServiceConfig2A
 - winsvc/ChangeServiceConfig2A
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
 - API-MS-Win-Service-management-l2-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - ChangeServiceConfig2
 - ChangeServiceConfig2A
 - ChangeServiceConfig2W
---

# ChangeServiceConfig2A function


## -description

Changes the optional configuration parameters of a service.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function and must have the <b>SERVICE_CHANGE_CONFIG</b> access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>. 




If the service controller handles the <b>SC_ACTION_RESTART</b> action, <i>hService</i> must have the <b>SERVICE_START</b> access right.

### -param dwInfoLevel [in]

The configuration information to be changed. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_DELAYED_AUTO_START_INFO"></a><a id="service_config_delayed_auto_start_info"></a><dl>
<dt><b>SERVICE_CONFIG_DELAYED_AUTO_START_INFO</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info">SERVICE_DELAYED_AUTO_START_INFO</a> structure.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_DESCRIPTION"></a><a id="service_config_description"></a><dl>
<dt><b>SERVICE_CONFIG_DESCRIPTION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_descriptiona">SERVICE_DESCRIPTION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_FAILURE_ACTIONS"></a><a id="service_config_failure_actions"></a><dl>
<dt><b>SERVICE_CONFIG_FAILURE_ACTIONS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actionsa">SERVICE_FAILURE_ACTIONS</a> structure.

If the service controller handles the <b>SC_ACTION_REBOOT</b> action, the caller must have the <b>SE_SHUTDOWN_NAME</b><a href="/windows/desktop/SecAuthZ/privileges"> privilege</a>. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_FAILURE_ACTIONS_FLAG"></a><a id="service_config_failure_actions_flag"></a><dl>
<dt><b>SERVICE_CONFIG_FAILURE_ACTIONS_FLAG</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actions_flag">SERVICE_FAILURE_ACTIONS_FLAG</a> structure.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_PREFERRED_NODE"></a><a id="service_config_preferred_node"></a><dl>
<dt><b>SERVICE_CONFIG_PREFERRED_NODE</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_preferred_node_info">SERVICE_PREFERRED_NODE_INFO</a> structure.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_PRESHUTDOWN_INFO"></a><a id="service_config_preshutdown_info"></a><dl>
<dt><b>SERVICE_CONFIG_PRESHUTDOWN_INFO</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_preshutdown_info">SERVICE_PRESHUTDOWN_INFO</a> structure.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO"></a><a id="service_config_required_privileges_info"></a><dl>
<dt><b>SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_required_privileges_infoa">SERVICE_REQUIRED_PRIVILEGES_INFO</a> structure.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_SERVICE_SID_INFO"></a><a id="service_config_service_sid_info"></a><dl>
<dt><b>SERVICE_CONFIG_SERVICE_SID_INFO</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_sid_info">SERVICE_SID_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_TRIGGER_INFO"></a><a id="service_config_trigger_info"></a><dl>
<dt><b>SERVICE_CONFIG_TRIGGER_INFO</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info">SERVICE_TRIGGER_INFO</a> structure. This value is not supported by the ANSI version of <b>ChangeServiceConfig2</b>. 

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_LAUNCH_PROTECTED"></a><a id="service_config_launch_protected"></a><dl>
<dt><b>SERVICE_CONFIG_LAUNCH_PROTECTED</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_launch_protected_info">SERVICE_LAUNCH_PROTECTED_INFO</a> structure.

<div class="alert"><b>Note</b>  This value is supported starting with Windows 8.1.</div>
<div> </div>
</td>
</tr>
</table>

### -param lpInfo [in, optional]

A pointer to the new value to be set for the configuration information. The format of this data depends on the value of the <i>dwInfoLevel</i> parameter. If this value is <b>NULL</b>, the information remains unchanged.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>ChangeServiceConfig2</b> function changes the optional configuration information for the specified service in the service control manager database. You can obtain the current optional configuration information by using the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a> function.

You cannot set the <b>SERVICE_CONFIG_FAILURE_ACTIONS</b> value for a service that shares the service control manager's process. This includes all services whose executable image is "Services.exe".

You can change and query additional configuration information using the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a> and 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a> functions, respectively.

If a service is configured to restart after it finishes with an error, the service control manager queues the restart action to occur after the specified time delay. A queued restart action cannot be canceled. If the service is manually restarted and then stopped before the queued restart action occurs, the service will restart unexpectedly when the time delay elapses. The service must be explicitly disabled to prevent it from restarting.

The <b>SERVICE_CONFIG_LAUNCH_PROTECTED</b> value can be used to launch the service as protected. In order to launch the service as protected, the service must be signed with a special certificate. 


SERVICE_CONFIG_LAUNCH_PROTECTED example:


```cpp
SERVICE_LAUNCH_PROTECTED_INFO Info;
SC_HANDLE hService;

Info.dwLaunchProtected = SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT;

hService = CreateService (...);

if (ChangeServiceConfig2(hService, 
                        SERVICE_CONFIG_LAUNCH_PROTECTED,
                        &Info) == FALSE)
{
    Result = GetLastError();
}

```



#### Examples

For an example, see 
<a href="/windows/desktop/Services/changing-a-service-configuration">Changing a Service's Configuration</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines ChangeServiceConfig2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicedynamicinformation">QueryServiceDynamicInformation</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info">SERVICE_DELAYED_AUTO_START_INFO</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_descriptiona">SERVICE_DESCRIPTION</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actionsa">SERVICE_FAILURE_ACTIONS</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actions_flag">SERVICE_FAILURE_ACTIONS_FLAG</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_preshutdown_info">SERVICE_PRESHUTDOWN_INFO</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_required_privileges_infoa">SERVICE_REQUIRED_PRIVILEGES_INFO</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_sid_info">SERVICE_SID_INFO</a>



<a href="/windows/desktop/Services/service-configuration">Service Configuration</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>
