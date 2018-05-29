---
UID: NS:mprapi._MPRAPI_TUNNEL_CONFIG_PARAMS0
title: "_MPRAPI_TUNNEL_CONFIG_PARAMS0"
author: windows-sdk-content
description: Used to get or set configuration of tunnel parameters on a RAS Server.
old-location: rras\mprapi_tunnel_config_params.htm
old-project: RRAS
ms.assetid: 19ad3493-99b7-405f-9663-3886388b5640
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PMPRAPI_TUNNEL_CONFIG_PARAMS0, MPRAPI_TUNNEL_CONFIG_PARAMS, MPRAPI_TUNNEL_CONFIG_PARAMS structure [RAS], MPRAPI_TUNNEL_CONFIG_PARAMS0, PMPRAPI_TUNNEL_CONFIG_PARAMS, PMPRAPI_TUNNEL_CONFIG_PARAMS structure pointer [RAS], _MPRAPI_TUNNEL_CONFIG_PARAMS0, _MPRAPI_TUNNEL_CONFIG_PARAMS1, mprapi/MPRAPI_TUNNEL_CONFIG_PARAMS, mprapi/PMPRAPI_TUNNEL_CONFIG_PARAMS, rras.mprapi_tunnel_config_params"
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
req.typenames: MPRAPI_TUNNEL_CONFIG_PARAMS0, *PMPRAPI_TUNNEL_CONFIG_PARAMS0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mprapi.h
api_name:
-	MPRAPI_TUNNEL_CONFIG_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MPRAPI_TUNNEL_CONFIG_PARAMS0 structure


## -description


The <b>MPRAPI_TUNNEL_CONFIG_PARAMS</b> structure is  used to get or set configuration of tunnel parameters on a RAS Server.


## -struct-fields




### -field IkeConfigParams

A <a href="https://msdn.microsoft.com/a494deb0-8f55-46cc-9ca0-a2097459de8b">IKEV2_CONFIG_PARAMS</a> structure that contains Internet Key Exchange version 2 (IKEv2) tunnel parameters.


### -field PptpConfigParams

A <a href="https://msdn.microsoft.com/0314c517-75be-4357-90bf-8a2a72d49542">PPTP_CONFIG_PARAMS</a> structure that contains Point-to-Point Tunneling Protocol (PPTP) tunnel parameters.


### -field L2tpConfigParams

A <a href="https://msdn.microsoft.com/7459054f-62c6-4ead-b969-884efc75ea80">L2TP_CONFIG_PARAMS</a> structure that contains Layer 2 Tunneling Protocol (L2TP) tunnel parameters.


### -field SstpConfigParams

A <a href="https://msdn.microsoft.com/6f21d569-af9b-49ba-ab02-4dfc74e87ed2">SSTP_CONFIG_PARAMS</a> structure that contains Secure Socket Tunneling Protocol (SSTP) tunnel parameters.


## -see-also




<a href="https://msdn.microsoft.com/6c993c9c-4522-4758-926a-fa7ef2a89418">MPR_SERVER_SET_CONFIG_EX</a>



<a href="https://msdn.microsoft.com/61265bb0-7884-4896-a76a-a2cc11ccccda">Router Management Enumerated Types</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

