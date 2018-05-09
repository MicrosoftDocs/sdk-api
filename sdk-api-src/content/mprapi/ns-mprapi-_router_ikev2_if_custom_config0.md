---
UID: NS:mprapi._ROUTER_IKEv2_IF_CUSTOM_CONFIG0
title: "_ROUTER_IKEv2_IF_CUSTOM_CONFIG0"
author: windows-driver-content
description: Gets or sets IKEv2 tunnel configuration parameter for IKEv2 tunnel based demand dial interfaces.
old-location: rras\router_ikev2_if_custom_config0.htm
old-project: RRAS
ms.assetid: c81611c6-3bad-4965-b4fb-b2c8074cee28
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PROUTER_IKEv2_IF_CUSTOM_CONFIG0, PROUTER_IKEv2_IF_CUSTOM_CONFIG0, PROUTER_IKEv2_IF_CUSTOM_CONFIG0 structure pointer [RAS], ROUTER_IKEv2_IF_CUSTOM_CONFIG0, ROUTER_IKEv2_IF_CUSTOM_CONFIG0 structure [RAS], _ROUTER_IKEv2_IF_CUSTOM_CONFIG0, mprapi/PROUTER_IKEv2_IF_CUSTOM_CONFIG0, mprapi/ROUTER_IKEv2_IF_CUSTOM_CONFIG0, rras.router_ikev2_if_custom_config0"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROUTER_IKEv2_IF_CUSTOM_CONFIG0, *PROUTER_IKEv2_IF_CUSTOM_CONFIG0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mprapi.h
api_name:
-	ROUTER_IKEv2_IF_CUSTOM_CONFIG0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ROUTER_IKEv2_IF_CUSTOM_CONFIG0 structure


## -description


Gets or sets IKEv2 tunnel configuration parameter for IKEv2 tunnel based demand dial interfaces. 

Do not use the <b>ROUTER_IKEv2_IF_CUSTOM_CONFIG0</b> structure directly in your code; using <a href="https://msdn.microsoft.com/6CF919BD-E1E9-423F-8186-C992A5E6AB89">ROUTER_IKEv2_IF_CUSTOM_CONFIG</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.


## -struct-fields




### -field dwSaLifeTime

A value that specifies the lifetime of a security association (SA) after which the SA is no longer valid.  This value must be between 300 and 17,279,999 seconds.


### -field dwSaDataSize

A value that specifies the number of kilobytes that are allowed to transfer using a SA. Afterwards, the SA will be renegotiated. This value must be greater than or equal to 1024 KB.


### -field certificateName

A value that specifies the configured certificate that will be sent to the peer for authentication during the main mode SA negotiation for the IKE2 tunnel based VPN connections.


### -field customPolicy

A value that specifies the custom IKEv2 configurations that will be used during  the SA negotiation. If set to <b>NULL</b>, no custom IKEv2configuration is available.

