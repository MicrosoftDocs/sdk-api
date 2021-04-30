---
UID: NS:rectypes.tagLINE_SEGMENT
title: LINE_SEGMENT (rectypes.h)
description: Describes the start and end points of a line recognition segment, such as the baseline or midline.
helpviewer_keywords: ["LINE_SEGMENT","LINE_SEGMENT structure [Tablet PC]","e9d4079d-28d2-4975-a33f-1f4ec5175c36","rectypes/LINE_SEGMENT","tablet.line_segment"]
old-location: tablet\line_segment.htm
tech.root: tablet
ms.assetid: e9d4079d-28d2-4975-a33f-1f4ec5175c36
ms.date: 12/05/2018
ms.keywords: LINE_SEGMENT, LINE_SEGMENT structure [Tablet PC], e9d4079d-28d2-4975-a33f-1f4ec5175c36, rectypes/LINE_SEGMENT, tablet.line_segment
req.header: rectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: LINE_SEGMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLINE_SEGMENT
 - rectypes/tagLINE_SEGMENT
 - LINE_SEGMENT
 - rectypes/LINE_SEGMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - LINE_SEGMENT
---

# LINE_SEGMENT structure


## -description

Describes the start and end points of a line recognition segment, such as the baseline or midline.

## -struct-fields

### -field PtA

Point that represents the start of the line segment. The point is in ink space coordinates.

### -field PtB

Point that represents the end of the line segment. The point is in ink space coordinates.

## -see-also

[LINE_METRICS Enumeration](./ne-rectypes-line_metrics.md)