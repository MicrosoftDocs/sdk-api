---
UID: NS:mprapi._L2TP_CONFIG_PARAMS0
title: "_L2TP_CONFIG_PARAMS0"
author: windows-sdk-content
description: Used to get and set the device configuration for Layer 2 Tunneling Protocool (L2TP) on a RAS Server.
old-location: rras\l2tp_config_params.htm
tech.root: RRAS
ms.assetid: 7459054f-62c6-4ead-b969-884efc75ea80
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PL2TP_CONFIG_PARAMS0, L2TP_CONFIG_PARAMS, L2TP_CONFIG_PARAMS structure [RAS], L2TP_CONFIG_PARAMS0, MPR_ENABLE_RAS_ON_DEVICE, MPR_ENABLE_ROUTING_ON_DEVICE, _L2TP_CONFIG_PARAMS0, _L2TP_CONFIG_PARAMS1, mprapi/L2TP_CONFIG_PARAMS, rras.l2tp_config_params"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - L2TP_CONFIG_PARAMS
product: Windows
targetos: Windows
req.typenames: L2TP_CONFIG_PARAMS0, *PL2TP_CONFIG_PARAMS0
req.redist: 
---

# _L2TP_CONFIG_PARAMS0 structure


## -description


The <b>L2TP_CONFIG_PARAMS</b> structure is used to get and set the device configuration for Layer 2 Tunneling Protocool (L2TP) on a RAS Server.


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
Windows Server 2008 Datacenterand Windows Server 2008 Enterprise

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If <b>dwNumPorts</b> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="https://msdn.microsoft.com/654d1410-b54c-4284-bf7f-f6ae6b7ef85e">MprConfigServerGetInfoEx</a> and <a href="https://msdn.microsoft.com/8251f391-7697-4024-9a9d-c7c810129a78">MprConfigServerSetInfoEx</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.</div>
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




<a href="https://msdn.microsoft.com/19ad3493-99b7-405f-9663-3886388b5640">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

