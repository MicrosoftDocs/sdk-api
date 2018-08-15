---
UID: NF:winsvc.QueryServiceConfig2W
title: QueryServiceConfig2W function
author: windows-sdk-content
description: Retrieves the optional configuration parameters of the specified service.
old-location: base\queryserviceconfig2.htm
old-project: services
ms.assetid: cb090e59-aeff-4420-bb7c-912a4911006f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: QueryServiceConfig2, QueryServiceConfig2 function, QueryServiceConfig2A, QueryServiceConfig2W, SERVICE_CONFIG_DELAYED_AUTO_START_INFO, SERVICE_CONFIG_DESCRIPTION, SERVICE_CONFIG_FAILURE_ACTIONS, SERVICE_CONFIG_FAILURE_ACTIONS_FLAG, SERVICE_CONFIG_LAUNCH_PROTECTED, SERVICE_CONFIG_PREFERRED_NODE, SERVICE_CONFIG_PRESHUTDOWN_INFO, SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO, SERVICE_CONFIG_SERVICE_SID_INFO, SERVICE_CONFIG_TRIGGER_INFO, _win32_queryserviceconfig2, base.queryserviceconfig2, winsvc/QueryServiceConfig2, winsvc/QueryServiceConfig2A, winsvc/QueryServiceConfig2W
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryServiceConfig2W (Unicode) and QueryServiceConfig2A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
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
 - QueryServiceConfig2
 - QueryServiceConfig2A
 - QueryServiceConfig2W
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# QueryServiceConfig2W function


## -description


Retrieves the optional configuration parameters of the specified service.


## -parameters




### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function and must have the <b>SERVICE_QUERY_CONFIG</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


### -param dwInfoLevel [in]

The configuration information to be queried. This parameter can be one of the following values.

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
The <i>lpBuffer</i> parameter is a pointer to a 
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
The <i>lpBuffer</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee">SERVICE_FAILURE_ACTIONS</a> structure.

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

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONFIG_TRIGGER_INFO"></a><a id="service_config_trigger_info"></a><dl>
<dt><b>SERVICE_CONFIG_TRIGGER_INFO</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The <i>lpInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/8de46056-1ea5-46f2-a260-ad140fd77bc1">SERVICE_TRIGGER_INFO</a> structure.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

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
 


### -param lpBuffer [out, optional]

A pointer to the buffer that receives the service configuration information. The format of this data depends on the value of the <i>dwInfoLevel</i> parameter.

The maximum size of this array is 8K bytes. To determine the required size, specify <b>NULL</b> for this parameter and 0 for the <i>cbBufSize</i> parameter. The function fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>. The <i>pcbBytesNeeded</i> parameter receives the needed size.


### -param cbBufSize [in]

The size of the structure pointed to by the <i>lpBuffer</i> parameter, in bytes.


### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes required to store the configuration information, if the function fails with  <b>ERROR_INSUFFICIENT_BUFFER</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
The handle does not have the <b>SERVICE_QUERY_CONFIG</b> access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
There is more service configuration information than would fit into the <i>lpBuffer</i> buffer. The number of bytes required to get all the information is returned in the <i>pcbBytesNeeded</i> parameter. Nothing is written to <i>lpBuffer</i>.

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
<b>QueryServiceConfig2</b> function returns the optional configuration information stored in the service control manager database for the specified service. You can change this configuration information by using the 
<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a> function.

You can change and query additional configuration information using the 
<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a> and 
<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a> functions, respectively.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/e6633dc9-c9b6-457d-8adc-e751ec9cf71d">Querying a Service's Configuration</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>



<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a>



<a href="https://msdn.microsoft.com/499b63fd-e77b-4b90-9ee7-ff4b7b12c431">QueryServiceDynamicInformation</a>



<a href="https://msdn.microsoft.com/5d95945f-f11b-42af-b302-8d924917b9ab">QueryServiceObjectSecurity</a>



<a href="https://msdn.microsoft.com/16117450-eb73-47de-8be7-c7aff3d44c81">SERVICE_DELAYED_AUTO_START_INFO</a>



<a href="https://msdn.microsoft.com/1b4e18d5-6086-4d1b-b39c-1d919bfdc0b9">SERVICE_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee">SERVICE_FAILURE_ACTIONS</a>



<a href="https://msdn.microsoft.com/49736b26-9565-4d56-abcd-1585b692ff12">SERVICE_FAILURE_ACTIONS_FLAG</a>



<a href="https://msdn.microsoft.com/b9d2362c-e4d7-4072-88c2-5294b3838095">SERVICE_PRESHUTDOWN_INFO</a>



<a href="https://msdn.microsoft.com/15a2e042-cfd5-443e-a3b8-822f48eb9654">SERVICE_REQUIRED_PRIVILEGES_INFO</a>



<a href="https://msdn.microsoft.com/cb1a32bd-aafb-4e41-8d6f-673c3d747f14">SERVICE_SID_INFO</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

