---
UID: NS:mprapi._PPTP_CONFIG_PARAMS
title: "_PPTP_CONFIG_PARAMS"
author: windows-sdk-content
description: Used to get and set the device configuration for Point-to-Point Tunneling Protocool (PPTP) on a RAS Server.
old-location: rras\pptp_config_params.htm
old-project: RRAS
ms.assetid: 0314c517-75be-4357-90bf-8a2a72d49542
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PPPTP_CONFIG_PARAMS, MPR_ENABLE_RAS_ON_DEVICE, MPR_ENABLE_ROUTING_ON_DEVICE, PPPTP_CONFIG_PARAMS, PPPTP_CONFIG_PARAMS structure pointer [RAS], PPTP_CONFIG_PARAMS, PPTP_CONFIG_PARAMS structure [RAS], _PPTP_CONFIG_PARAMS, mprapi/PPPTP_CONFIG_PARAMS, mprapi/PPTP_CONFIG_PARAMS, rras.pptp_config_params"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PPTP_CONFIG_PARAMS, *PPPTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPTP_CONFIG_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _PPTP_CONFIG_PARAMS structure


## -description


The <b>PPTP_CONFIG_PARAMS</b> structure is used to get and set the device configuration for Point-to-Point Tunneling Protocool (PPTP) on a RAS Server.


## -struct-fields




### -field dwNumPorts

A value that specifies the number of ports configured on the RRAS server to accept PPTP connections. The maximum values for <b>dwNumPorts</b> are listed in the following table. The value zero is not allowed.

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

A value that specifies the type of ports configured on the  RRAS server for PPTP. The following values are supported:

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
 

 

