---
UID: NS:mprapi._IKEV2_CONFIG_PARAMS
title: IKEV2_CONFIG_PARAMS (mprapi.h)
description: Used to get or set parameters for Internet Key Exchange version 2 (IKEv2) devices (RFC 4306).
helpviewer_keywords: ["*PIKEV2_CONFIG_PARAMS","IKEV2_CONFIG_PARAMS","IKEV2_CONFIG_PARAMS structure [RAS]","MPRAPI_IKEV2_SET_TUNNEL_CONFIG_PARAMS","MPR_ENABLE_RAS_ON_DEVICE","PIKEV2_CONFIG_PARAMS","PIKEV2_CONFIG_PARAMS structure pointer [RAS]","mprapi/IKEV2_CONFIG_PARAMS","mprapi/PIKEV2_CONFIG_PARAMS","rras.ikev2_config_params"]
old-location: rras\ikev2_config_params.htm
tech.root: RRAS
ms.assetid: a494deb0-8f55-46cc-9ca0-a2097459de8b
ms.date: 12/05/2018
ms.keywords: '*PIKEV2_CONFIG_PARAMS, IKEV2_CONFIG_PARAMS, IKEV2_CONFIG_PARAMS structure [RAS], MPRAPI_IKEV2_SET_TUNNEL_CONFIG_PARAMS, MPR_ENABLE_RAS_ON_DEVICE, PIKEV2_CONFIG_PARAMS, PIKEV2_CONFIG_PARAMS structure pointer [RAS], mprapi/IKEV2_CONFIG_PARAMS, mprapi/PIKEV2_CONFIG_PARAMS, rras.ikev2_config_params'
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
req.typenames: IKEV2_CONFIG_PARAMS, *PIKEV2_CONFIG_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IKEV2_CONFIG_PARAMS
 - mprapi/_IKEV2_CONFIG_PARAMS
 - PIKEV2_CONFIG_PARAMS
 - mprapi/PIKEV2_CONFIG_PARAMS
 - IKEV2_CONFIG_PARAMS
 - mprapi/IKEV2_CONFIG_PARAMS
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
 - IKEV2_CONFIG_PARAMS
---

# IKEV2_CONFIG_PARAMS structure


## -description

The <b>IKEV2_CONFIG_PARAMS</b> structure is used to get or set parameters for Internet Key Exchange version 2 (IKEv2) devices (<a href="https://www.ietf.org/rfc/rfc4306.txt">RFC 4306</a>).

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

An <a href="/windows/desktop/RRAS/router-management-data-types">IKEV2_TUNNEL_CONFIG_PARAMS</a> structure that contains IKEv2 tunnel information.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_tunnel_config_params0">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>