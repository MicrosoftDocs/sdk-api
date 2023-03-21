---
UID: NS:mprapi._L2TP_CONFIG_PARAMS0
title: L2TP_CONFIG_PARAMS0 (mprapi.h)
description: Used to get and set the device configuration for Layer 2 Tunneling Protocol (L2TP) on a RAS Server. (L2TP_CONFIG_PARAMS0)
helpviewer_keywords: ["*PL2TP_CONFIG_PARAMS0","L2TP_CONFIG_PARAMS","L2TP_CONFIG_PARAMS structure [RAS]","L2TP_CONFIG_PARAMS0","L2TP_CONFIG_PARAMS1","MPR_ENABLE_RAS_ON_DEVICE","MPR_ENABLE_ROUTING_ON_DEVICE","_L2TP_CONFIG_PARAMS0","_L2TP_CONFIG_PARAMS1","mprapi/L2TP_CONFIG_PARAMS","rras.l2tp_config_params"]
old-location: rras\l2tp_config_params.htm
tech.root: RRAS
ms.assetid: 7459054f-62c6-4ead-b969-884efc75ea80
ms.date: 12/05/2018
ms.keywords: '*PL2TP_CONFIG_PARAMS0, L2TP_CONFIG_PARAMS, L2TP_CONFIG_PARAMS structure [RAS], L2TP_CONFIG_PARAMS0, L2TP_CONFIG_PARAMS1, MPR_ENABLE_RAS_ON_DEVICE, MPR_ENABLE_ROUTING_ON_DEVICE, _L2TP_CONFIG_PARAMS0, _L2TP_CONFIG_PARAMS1, mprapi/L2TP_CONFIG_PARAMS, rras.l2tp_config_params'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: L2TP_CONFIG_PARAMS0, *PL2TP_CONFIG_PARAMS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _L2TP_CONFIG_PARAMS0
 - mprapi/_L2TP_CONFIG_PARAMS0
 - PL2TP_CONFIG_PARAMS0
 - mprapi/PL2TP_CONFIG_PARAMS0
 - L2TP_CONFIG_PARAMS0
 - mprapi/L2TP_CONFIG_PARAMS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - L2TP_CONFIG_PARAMS
 - L2TP_CONFIG_PARAMS0
 - L2TP_CONFIG_PARAMS1
---

# L2TP_CONFIG_PARAMS0 structure


## -description

The <b>L2TP_CONFIG_PARAMS</b> structure is used to get and set the device configuration for Layer 2 Tunneling Protocol (L2TP) on a RAS Server.

## -struct-fields

### -field dwNumPorts

A value that specifies the number of ports configured on the RRAS server to accept L2TP connections. The maximum values for <b>dwNumPorts</b> are listed in the following table. The value zero is not allowed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Windows Web Server 2008

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Standard

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>30000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Datacenter and Windows Server 2008 Enterprise

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If <b>dwNumPorts</b> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigservergetinfoex">MprConfigServerGetInfoEx</a> and <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfoex">MprConfigServerSetInfoEx</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.</div>
<div> </div>

### -field dwPortFlags

A value that specifies the type of ports configured on the  RRAS server for L2TP. The following values are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPR_ENABLE_RAS_ON_DEVICE"></a><a id="mpr_enable_ras_on_device"></a><dl>
<dt><b>MPR_ENABLE_RAS_ON_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, RAS is enabled on the device.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_ENABLE_ROUTING_ON_DEVICE"></a><a id="mpr_enable_routing_on_device"></a><dl>
<dt><b>MPR_ENABLE_ROUTING_ON_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, routing is enabled on the device.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_tunnel_config_params0">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>
