---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

