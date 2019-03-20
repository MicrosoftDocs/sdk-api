---
UID: NF:winsvc.ChangeServiceConfig2A
title: ChangeServiceConfig2A function (winsvc.h)
author: windows-sdk-content
description: Changes the optional configuration parameters of a service.
old-location: base\changeserviceconfig2.htm
tech.root: Services
ms.assetid: 6e5b79ed-52e1-460e-b076-01afbd08775c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ChangeServiceConfig2, ChangeServiceConfig2 function, ChangeServiceConfig2A, ChangeServiceConfig2W, SERVICE_CONFIG_DELAYED_AUTO_START_INFO, SERVICE_CONFIG_DESCRIPTION, SERVICE_CONFIG_FAILURE_ACTIONS, SERVICE_CONFIG_FAILURE_ACTIONS_FLAG, SERVICE_CONFIG_LAUNCH_PROTECTED, SERVICE_CONFIG_PREFERRED_NODE, SERVICE_CONFIG_PRESHUTDOWN_INFO, SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO, SERVICE_CONFIG_SERVICE_SID_INFO, SERVICE_CONFIG_TRIGGER_INFO, _win32_changeserviceconfig2, base.changeserviceconfig2, winsvc/ChangeServiceConfig2, winsvc/ChangeServiceConfig2A, winsvc/ChangeServiceConfig2W
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ChangeServiceConfig2A function


## -description


Changes the optional configuration parameters of a service.


## -parameters




### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function and must have the <b>SERVICE_CHANGE_CONFIG</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>. 




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
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/16117450-eb73-47de-8be7-c7aff3d44c81">SERVICE_DELAYED_AUTO_START_INFO</a> structure.

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
<a href="https://msdn.microsoft.com/1b4e18d5-6086-4d1b-b39c-1d919bfdc0b9">SERVICE_DESCRIPTION</a> structure.

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
<a href="https://msdn.microsoft.com/180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee">SERVICE_FAILURE_ACTIONS</a> structure.

If the service controller handles the <b>SC_ACTION_REBOOT</b> action, the caller must have the <b>SE_SHUTDOWN_NAME</b><a href="https://msdn.microsoft.com/fe6aae0f-93eb-4aba-a6ac-45e71c251c51"> privilege</a>. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_FAILURE_ACTIONS_FLAG"></a><a id="service_config_failure_actions_flag"></a><dl>
<dt><b>SERVICE_CONFIG_FAILURE_ACTIONS_FLAG</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/49736b26-9565-4d56-abcd-1585b692ff12">SERVICE_FAILURE_ACTIONS_FLAG</a> structure.

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
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/aa16cc56-0a95-47e0-9390-c219b83aeeb4">SERVICE_PREFERRED_NODE_INFO</a> structure.

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
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/b9d2362c-e4d7-4072-88c2-5294b3838095">SERVICE_PRESHUTDOWN_INFO</a> structure.

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
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/15a2e042-cfd5-443e-a3b8-822f48eb9654">SERVICE_REQUIRED_PRIVILEGES_INFO</a> structure.

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
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/cb1a32bd-aafb-4e41-8d6f-673c3d747f14">SERVICE_SID_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_TRIGGER_INFO"></a><a id="service_config_trigger_info"></a><dl>
<dt><b>SERVICE_CONFIG_TRIGGER_INFO</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/8de46056-1ea5-46f2-a260-ad140fd77bc1">SERVICE_TRIGGER_INFO</a> structure. This value is not supported by the ANSI version of <b>ChangeServiceConfig2</b>. 

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
The <i>lpInfo</i> parameter is a pointer a <a href="https://msdn.microsoft.com/ECD44E9F-BE48-4038-94B4-37C8CA5C89F7">SERVICE_LAUNCH_PROTECTED_INFO</a> structure.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>ChangeServiceConfig2</b> function changes the optional configuration information for the specified service in the service control manager database. You can obtain the current optional configuration information by using the 
<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a> function.

You cannot set the <b>SERVICE_CONFIG_FAILURE_ACTIONS</b> value for a service that shares the service control manager's process. This includes all services whose executable image is "Services.exe".

You can change and query additional configuration information using the 
<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a> and 
<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a> functions, respectively.

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
<a href="https://msdn.microsoft.com/79aa4ad5-87ee-4f5d-9c8e-4e788f4c7182">Changing a Service's Configuration</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/499b63fd-e77b-4b90-9ee7-ff4b7b12c431">QueryServiceDynamicInformation</a>



<a href="https://msdn.microsoft.com/16117450-eb73-47de-8be7-c7aff3d44c81">SERVICE_DELAYED_AUTO_START_INFO</a>



<a href="https://msdn.microsoft.com/1b4e18d5-6086-4d1b-b39c-1d919bfdc0b9">SERVICE_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee">SERVICE_FAILURE_ACTIONS</a>



<a href="https://msdn.microsoft.com/49736b26-9565-4d56-abcd-1585b692ff12">SERVICE_FAILURE_ACTIONS_FLAG</a>



<a href="https://msdn.microsoft.com/b9d2362c-e4d7-4072-88c2-5294b3838095">SERVICE_PRESHUTDOWN_INFO</a>



<a href="https://msdn.microsoft.com/15a2e042-cfd5-443e-a3b8-822f48eb9654">SERVICE_REQUIRED_PRIVILEGES_INFO</a>



<a href="https://msdn.microsoft.com/cb1a32bd-aafb-4e41-8d6f-673c3d747f14">SERVICE_SID_INFO</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

