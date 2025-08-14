---
UID: NF:winsvc.QueryServiceConfig2A
title: QueryServiceConfig2A function (winsvc.h)
description: Retrieves the optional configuration parameters of the specified service. (ANSI)
helpviewer_keywords: ["QueryServiceConfig2A", "SERVICE_CONFIG_DELAYED_AUTO_START_INFO", "SERVICE_CONFIG_DESCRIPTION", "SERVICE_CONFIG_FAILURE_ACTIONS", "SERVICE_CONFIG_FAILURE_ACTIONS_FLAG", "SERVICE_CONFIG_LAUNCH_PROTECTED", "SERVICE_CONFIG_PREFERRED_NODE", "SERVICE_CONFIG_PRESHUTDOWN_INFO", "SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO", "SERVICE_CONFIG_SERVICE_SID_INFO", "SERVICE_CONFIG_TRIGGER_INFO", "winsvc/QueryServiceConfig2A"]
old-location: base\queryserviceconfig2.htm
tech.root: security
ms.assetid: cb090e59-aeff-4420-bb7c-912a4911006f
ms.date: 12/05/2018
ms.keywords: QueryServiceConfig2, QueryServiceConfig2 function, QueryServiceConfig2A, QueryServiceConfig2W, SERVICE_CONFIG_DELAYED_AUTO_START_INFO, SERVICE_CONFIG_DESCRIPTION, SERVICE_CONFIG_FAILURE_ACTIONS, SERVICE_CONFIG_FAILURE_ACTIONS_FLAG, SERVICE_CONFIG_LAUNCH_PROTECTED, SERVICE_CONFIG_PREFERRED_NODE, SERVICE_CONFIG_PRESHUTDOWN_INFO, SERVICE_CONFIG_REQUIRED_PRIVILEGES_INFO, SERVICE_CONFIG_SERVICE_SID_INFO, SERVICE_CONFIG_TRIGGER_INFO, _win32_queryserviceconfig2, base.queryserviceconfig2, winsvc/QueryServiceConfig2, winsvc/QueryServiceConfig2A, winsvc/QueryServiceConfig2W
req.header: winsvc.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryServiceConfig2A
 - winsvc/QueryServiceConfig2A
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
 - QueryServiceConfig2
 - QueryServiceConfig2A
 - QueryServiceConfig2W
---

# QueryServiceConfig2A function


## -description

Retrieves the optional configuration parameters of the specified service.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function and must have the <b>SERVICE_QUERY_CONFIG</b> access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

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
The <i>lpBuffer</i> parameter is a pointer to a 
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
The <i>lpBuffer</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actionsa">SERVICE_FAILURE_ACTIONS</a> structure.

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
The <i>lpInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info">SERVICE_TRIGGER_INFO</a> structure.

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
The <i>lpInfo</i> parameter is a pointer a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_launch_protected_info">SERVICE_LAUNCH_PROTECTED_INFO</a> structure.

<div class="alert"><b>Note</b>  This value is supported starting with Windows 8.1.</div>
<div> </div>
</td>
</tr>
</table>

### -param lpBuffer [out, optional]

A pointer to the buffer that receives the service configuration information. The format of this data depends on the value of the <i>dwInfoLevel</i> parameter.

The maximum size of this array is 8K bytes. To determine the required size, specify <b>NULL</b> for this parameter and 0 for the <i>cbBufSize</i> parameter. The function fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>. The <i>pcbBytesNeeded</i> parameter receives the needed size.

### -param cbBufSize [in]

The size of the structure pointed to by the <i>lpBuffer</i> parameter, in bytes.

### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes required to store the configuration information, if the function fails with  <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a> function.

You can change and query additional configuration information using the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a> and 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a> functions, respectively.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/querying-a-service-s-configuration">Querying a Service's Configuration</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines QueryServiceConfig2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga">QueryServiceConfig</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicedynamicinformation">QueryServiceDynamicInformation</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity">QueryServiceObjectSecurity</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info">SERVICE_DELAYED_AUTO_START_INFO</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_descriptiona">SERVICE_DESCRIPTION</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actionsa">SERVICE_FAILURE_ACTIONS</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actions_flag">SERVICE_FAILURE_ACTIONS_FLAG</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_preshutdown_info">SERVICE_PRESHUTDOWN_INFO</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_required_privileges_infoa">SERVICE_REQUIRED_PRIVILEGES_INFO</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_sid_info">SERVICE_SID_INFO</a>



<a href="/windows/desktop/Services/service-configuration">Service Configuration</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>
