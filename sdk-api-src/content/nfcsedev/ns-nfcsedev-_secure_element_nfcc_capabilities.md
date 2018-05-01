---
UID: NS:nfcsedev._SECURE_ELEMENT_NFCC_CAPABILITIES
title: "_SECURE_ELEMENT_NFCC_CAPABILITIES"
author: windows-driver-content
description: SECURE_ELEMENT_NFCC_CAPABILITIES contains NFC controller capabilities.
old-location: nfpdrivers\_secure_element_nfcc_capabilities.htm
old-project: nfpdrivers
ms.assetid: D1F9588B-02D9-49B0-B45F-AF5C140D74E4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSECURE_ELEMENT_NFCC_CAPABILITIES, PSECURE_ELEMENT_NFCC_CAPABILITIES, P_SECURE_ELEMENT_NFCC_CAPABILITIES, P_SECURE_ELEMENT_NFCC_CAPABILITIES structure pointer [Near-Field Proximity Drivers], SECURE_ELEMENT_NFCC_CAPABILITIES, SECURE_ELEMENT_NFCC_CAPABILITIES structure [Near-Field Proximity Drivers], _SECURE_ELEMENT_NFCC_CAPABILITIES, nfcsedev/P_SECURE_ELEMENT_NFCC_CAPABILITIES, nfcsedev/_SECURE_ELEMENT_NFCC_CAPABILITIES, nfpdrivers._secure_element_nfcc_capabilities"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: nfcsedev.h
req.include-header: 
req.target-type: Windows
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
req.typenames: SECURE_ELEMENT_NFCC_CAPABILITIES, *PSECURE_ELEMENT_NFCC_CAPABILITIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nfcsedev.h
api_name:
-	SECURE_ELEMENT_NFCC_CAPABILITIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _SECURE_ELEMENT_NFCC_CAPABILITIES structure


## -description


SECURE_ELEMENT_NFCC_CAPABILITIES contains NFC controller capabilities. 


## -struct-fields




### -field cbMaxRoutingTableSize

NFCC maximum listen mode routing table size.


### -field IsAidRoutingSupported

Specifies whether NFCC supports AID-based routing.



### -field IsProtocolRoutingSupported

Specify whether NFCC supports protocol-based routing.


### -field IsTechRoutingSupported

Specify whether NFCC supports technology-based routing.

