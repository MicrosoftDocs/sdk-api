---
UID: NS:mprapi._MPRAPI_TUNNEL_CONFIG_PARAMS0
title: MPRAPI_TUNNEL_CONFIG_PARAMS0 (mprapi.h)
description: Used to get or set configuration of tunnel parameters on a RAS Server. (MPRAPI_TUNNEL_CONFIG_PARAMS0)
helpviewer_keywords: ["*PMPRAPI_TUNNEL_CONFIG_PARAMS0","MPRAPI_TUNNEL_CONFIG_PARAMS","MPRAPI_TUNNEL_CONFIG_PARAMS structure [RAS]","MPRAPI_TUNNEL_CONFIG_PARAMS0","MPRAPI_TUNNEL_CONFIG_PARAMS1","PMPRAPI_TUNNEL_CONFIG_PARAMS","PMPRAPI_TUNNEL_CONFIG_PARAMS structure pointer [RAS]","_MPRAPI_TUNNEL_CONFIG_PARAMS0","_MPRAPI_TUNNEL_CONFIG_PARAMS1","mprapi/MPRAPI_TUNNEL_CONFIG_PARAMS","mprapi/PMPRAPI_TUNNEL_CONFIG_PARAMS","rras.mprapi_tunnel_config_params"]
old-location: rras\mprapi_tunnel_config_params.htm
tech.root: RRAS
ms.assetid: 19ad3493-99b7-405f-9663-3886388b5640
ms.date: 12/05/2018
ms.keywords: '*PMPRAPI_TUNNEL_CONFIG_PARAMS0, MPRAPI_TUNNEL_CONFIG_PARAMS, MPRAPI_TUNNEL_CONFIG_PARAMS structure [RAS], MPRAPI_TUNNEL_CONFIG_PARAMS0, MPRAPI_TUNNEL_CONFIG_PARAMS1, PMPRAPI_TUNNEL_CONFIG_PARAMS, PMPRAPI_TUNNEL_CONFIG_PARAMS structure pointer [RAS], _MPRAPI_TUNNEL_CONFIG_PARAMS0, _MPRAPI_TUNNEL_CONFIG_PARAMS1, mprapi/MPRAPI_TUNNEL_CONFIG_PARAMS, mprapi/PMPRAPI_TUNNEL_CONFIG_PARAMS, rras.mprapi_tunnel_config_params'
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
req.typenames: MPRAPI_TUNNEL_CONFIG_PARAMS0, *PMPRAPI_TUNNEL_CONFIG_PARAMS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPRAPI_TUNNEL_CONFIG_PARAMS0
 - mprapi/_MPRAPI_TUNNEL_CONFIG_PARAMS0
 - PMPRAPI_TUNNEL_CONFIG_PARAMS0
 - mprapi/PMPRAPI_TUNNEL_CONFIG_PARAMS0
 - MPRAPI_TUNNEL_CONFIG_PARAMS0
 - mprapi/MPRAPI_TUNNEL_CONFIG_PARAMS0
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
 - MPRAPI_TUNNEL_CONFIG_PARAMS
 - MPRAPI_TUNNEL_CONFIG_PARAMS0
 - MPRAPI_TUNNEL_CONFIG_PARAMS1
---

# MPRAPI_TUNNEL_CONFIG_PARAMS0 structure


## -description

The <b>MPRAPI_TUNNEL_CONFIG_PARAMS</b> structure is  used to get or set configuration of tunnel parameters on a RAS Server.

## -struct-fields

### -field IkeConfigParams

A <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_config_params">IKEV2_CONFIG_PARAMS</a> structure that contains Internet Key Exchange version 2 (IKEv2) tunnel parameters.

### -field PptpConfigParams

A <a href="/windows/desktop/api/mprapi/ns-mprapi-pptp_config_params">PPTP_CONFIG_PARAMS</a> structure that contains Point-to-Point Tunneling Protocol (PPTP) tunnel parameters.

### -field L2tpConfigParams

A <a href="/windows/desktop/api/mprapi/ns-mprapi-l2tp_config_params0">L2TP_CONFIG_PARAMS</a> structure that contains Layer 2 Tunneling Protocol (L2TP) tunnel parameters.

### -field SstpConfigParams

A <a href="/windows/desktop/api/mprapi/ns-mprapi-sstp_config_params">SSTP_CONFIG_PARAMS</a> structure that contains Secure Socket Tunneling Protocol (SSTP) tunnel parameters.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_set_config_ex0">MPR_SERVER_SET_CONFIG_EX</a>



<a href="/windows/desktop/RRAS/router-management-enumerations">Router Management Enumerated Types</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
