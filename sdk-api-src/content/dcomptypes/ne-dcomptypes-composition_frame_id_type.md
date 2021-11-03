---
UID: NE:dcomptypes.COMPOSITION_FRAME_ID_TYPE
tech.root: directcomp
title: COMPOSITION_FRAME_ID_TYPE
ms.date: 06/24/2021
targetos: Windows
description: Defines constants that specify the status of a compositor frame.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: dcomptypes.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - COMPOSITION_FRAME_ID_TYPE
f1_keywords:
 - COMPOSITION_FRAME_ID_TYPE
 - dcomptypes/COMPOSITION_FRAME_ID_TYPE
dev_langs:
 - c++
---

## -description

Defines constants that specify the status of a compositor frame.

## -enum-fields

### -field COMPOSITION_FRAME_ID_CREATED

The compositor has started working on the frame.

### -field COMPOSITION_FRAME_ID_CONFIRMED

CPU work is completed and any presents have taken place.

### -field COMPOSITION_FRAME_ID_COMPLETED

GPU work is completed for all render targets associated with the frame.

## -remarks

## -see-also

