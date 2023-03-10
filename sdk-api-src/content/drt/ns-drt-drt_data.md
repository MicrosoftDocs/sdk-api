---
UID: NS:drt.drt_data_tag
title: DRT_DATA (drt.h)
description: DRT_DATA structure contains a data blob. This structure is used by several DRT functions.
helpviewer_keywords: ["*PDRT_DATA","DRT_DATA","DRT_DATA structure [Peer Networking]","PDRT_DATA","PDRT_DATA structure pointer [Peer Networking]","drt/DRT_DATA","drt/PDRT_DATA","p2p.drt_data"]
old-location: p2p\drt_data.htm
tech.root: p2p
ms.assetid: ee81daca-e889-471e-b43b-4593380a55dd
ms.date: 12/05/2018
ms.keywords: '*PDRT_DATA, DRT_DATA, DRT_DATA structure [Peer Networking], PDRT_DATA, PDRT_DATA structure pointer [Peer Networking], drt/DRT_DATA, drt/PDRT_DATA, p2p.drt_data'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DRT_DATA, *PDRT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - drt_data_tag
 - drt/drt_data_tag
 - PDRT_DATA
 - drt/PDRT_DATA
 - DRT_DATA
 - drt/DRT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_DATA
---

# DRT_DATA structure


## -description

The  <b>DRT_DATA</b> structure contains a data blob. This structure is used by several DRT functions.

## -struct-fields

### -field cb

The number of bytes.

### -field pb

Pointer to a byte array that contains the common data.

