---
UID: NS:drt.drt_data_tag
title: drt_data_tag
author: windows-driver-content
description: DRT_DATA structure contains a data blob. This structure is used by several DRT functions.
old-location: p2p\drt_data.htm
old-project: P2PSdk
ms.assetid: ee81daca-e889-471e-b43b-4593380a55dd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PDRT_DATA, DRT_DATA, DRT_DATA structure [Peer Networking], PDRT_DATA, PDRT_DATA structure pointer [Peer Networking], drt/DRT_DATA, drt/PDRT_DATA, drt_data_tag, p2p.drt_data"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.typenames: DRT_DATA, *PDRT_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	drt.h
api_name:
-	DRT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# drt_data_tag structure


## -description


The  <b>DRT_DATA</b> structure contains a data blob. This structure is used by several DRT functions.


## -struct-fields




### -field cb

The number of bytes.


### -field pb

Pointer to a byte array that contains the common data.

