---
UID: NS:nfcsedev._SECURE_ELEMENT_ROUTING_TABLE
title: "_SECURE_ELEMENT_ROUTING_TABLE"
author: windows-driver-content
description: SECURE_ELEMENT_ROUTING_TABLE is an input parameter for IOCTL_NFCSE_SET_ROUTING_TABLE.
old-location: nfpdrivers\_secure_element_routing_table.htm
old-project: nfpdrivers
ms.assetid: AD5E6434-BBBF-44CB-8153-B8F4D4F75E94
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSECURE_ELEMENT_ROUTING_TABLE, PSECURE_ELEMENT_ROUTING_TABLE, P_SECURE_ELEMENT_ROUTING_TABLE, P_SECURE_ELEMENT_ROUTING_TABLE structure pointer [Near-Field Proximity Drivers], SECURE_ELEMENT_ROUTING_TABLE, SECURE_ELEMENT_ROUTING_TABLE structure [Near-Field Proximity Drivers], _SECURE_ELEMENT_ROUTING_TABLE, nfcsedev/P_SECURE_ELEMENT_ROUTING_TABLE, nfcsedev/_SECURE_ELEMENT_ROUTING_TABLE, nfpdrivers._secure_element_routing_table"
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
req.typenames: SECURE_ELEMENT_ROUTING_TABLE, *PSECURE_ELEMENT_ROUTING_TABLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nfcsedev.h
api_name:
-	SECURE_ELEMENT_ROUTING_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _SECURE_ELEMENT_ROUTING_TABLE structure


## -description


SECURE_ELEMENT_ROUTING_TABLE is an input parameter for <a href="https://msdn.microsoft.com/library/windows/hardware/dn905513">IOCTL_NFCSE_SET_ROUTING_TABLE</a>.


## -struct-fields




### -field NumberOfEntries

Number of routing table entries.


### -field TableEntries

 




#### - TableEntries[ANYSIZE_ARRAY]

Listen mode routing table.

