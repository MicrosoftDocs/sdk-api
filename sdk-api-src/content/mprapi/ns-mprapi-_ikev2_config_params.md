---
UID: NS:mprapi._IKEV2_CONFIG_PARAMS
title: "_IKEV2_CONFIG_PARAMS"
author: windows-sdk-content
description: Used to get or set parameters for Internet Key Exchange version 2 (IKEv2) devices (RFC 4306).
old-location: rras\ikev2_config_params.htm
tech.root: RRAS
ms.assetid: a494deb0-8f55-46cc-9ca0-a2097459de8b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PIKEV2_CONFIG_PARAMS, IKEV2_CONFIG_PARAMS, IKEV2_CONFIG_PARAMS structure [RAS], MPRAPI_IKEV2_SET_TUNNEL_CONFIG_PARAMS, MPR_ENABLE_RAS_ON_DEVICE, PIKEV2_CONFIG_PARAMS, PIKEV2_CONFIG_PARAMS structure pointer [RAS], _IKEV2_CONFIG_PARAMS, mprapi/IKEV2_CONFIG_PARAMS, mprapi/PIKEV2_CONFIG_PARAMS, rras.ikev2_config_params"
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
 - IKEV2_CONFIG_PARAMS
product: Windows
targetos: Windows
req.typenames: IKEV2_CONFIG_PARAMS, *PIKEV2_CONFIG_PARAMS
req.redist: 
---

# _IKEV2_CONFIG_PARAMS structure


## -description


The <b>IKEV2_CONFIG_PARAMS</b> structure is used to get or set parameters for Internet Key Exchange version 2 (IKEv2) devices (<a href="Http://go.microsoft.com/fwlink/p/?linkid=90469">RFC 4306</a>).


## -struct-fields




### -field dwNumPorts

A value that specifies the number of ports configured on the RRAS server to accept IKEv2 connections.


### -field dwPortFlags

A value that specifies the type of ports configured on the  RRAS server for IKEv2. The following values are supported:

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
Remote Access is enabled for IKEv2.

</td>
</tr>
</table>
 


### -field dwTunnelConfigParamFlags

A value that specifies if the user is able to set the tunnel configuration parameters. The following values are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IKEV2_SET_TUNNEL_CONFIG_PARAMS"></a><a id="mprapi_ikev2_set_tunnel_config_params"></a><dl>
<dt><b>MPRAPI_IKEV2_SET_TUNNEL_CONFIG_PARAMS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
If set, the <b>dwNumPorts</b>, <b>dwPortFlags</b>, and <b>TunnelConfigParams</b> fields are valid.

</td>
</tr>
</table>
 


### -field TunnelConfigParams

An <a href="https://msdn.microsoft.com/6CF919BD-E1E9-423F-8186-C992A5E6AB89">IKEV2_TUNNEL_CONFIG_PARAMS</a> structure that contains IKEv2 tunnel information.


## -see-also




<a href="https://msdn.microsoft.com/19ad3493-99b7-405f-9663-3886388b5640">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

