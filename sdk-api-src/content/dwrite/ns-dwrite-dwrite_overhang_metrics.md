---
UID: NS:dwrite.DWRITE_OVERHANG_METRICS
title: DWRITE_OVERHANG_METRICS (dwrite.h)
description: Indicates how much any visible DIPs (device independent pixels) overshoot each side of the layout or inline objects.
helpviewer_keywords: ["DWRITE_OVERHANG_METRICS","DWRITE_OVERHANG_METRICS structure [Direct Write]","PDWRITE_OVERHANG_METRICS","PDWRITE_OVERHANG_METRICS structure pointer [Direct Write]","directwrite.dwrite_overhang_metrics","dwrite/DWRITE_OVERHANG_METRICS","dwrite/PDWRITE_OVERHANG_METRICS"]
old-location: directwrite\dwrite_overhang_metrics.htm
tech.root: DirectWrite
ms.assetid: a285f06b-a4d0-4ebe-80f5-157e59bfba31
ms.date: 12/05/2018
ms.keywords: DWRITE_OVERHANG_METRICS, DWRITE_OVERHANG_METRICS structure [Direct Write], PDWRITE_OVERHANG_METRICS, PDWRITE_OVERHANG_METRICS structure pointer [Direct Write], directwrite.dwrite_overhang_metrics, dwrite/DWRITE_OVERHANG_METRICS, dwrite/PDWRITE_OVERHANG_METRICS
req.header: dwrite.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_OVERHANG_METRICS
 - dwrite/DWRITE_OVERHANG_METRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_OVERHANG_METRICS
---

# DWRITE_OVERHANG_METRICS structure


## -description

Indicates how much any visible DIPs (device independent pixels) overshoot each side of the layout or inline objects.

Positive overhangs indicate that the visible area extends outside the layout box or inline object, while negative values mean there is whitespace inside.
 The returned values are unaffected by rendering transforms or pixel snapping.  Additionally, they may not exactly match the final target's pixel bounds after applying grid fitting and hinting.

## -struct-fields

### -field left

Type: <b>FLOAT</b>

The distance from the left-most visible DIP to its  left-alignment edge.

### -field top

Type: <b>FLOAT</b>

The distance from the top-most visible DIP to its  top alignment edge.

### -field right

Type: <b>FLOAT</b>

The distance from the right-most visible DIP to its  right-alignment edge.

### -field bottom

Type: <b>FLOAT</b>

The distance from the bottom-most visible DIP to its lower-alignment edge.

