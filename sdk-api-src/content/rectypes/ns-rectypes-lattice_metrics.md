---
UID: NS:rectypes.tagLATTICE_METRICS
title: LATTICE_METRICS (rectypes.h)
description: Describes the baseline and the midline height.
helpviewer_keywords: ["4fdeaaf9-9026-4bf1-8e78-d03a98d44b32","LATTICE_METRICS","LATTICE_METRICS structure [Tablet PC]","rectypes/LATTICE_METRICS","tablet.lattice_metrics"]
old-location: tablet\lattice_metrics.htm
tech.root: tablet
ms.assetid: 4fdeaaf9-9026-4bf1-8e78-d03a98d44b32
ms.date: 12/05/2018
ms.keywords: 4fdeaaf9-9026-4bf1-8e78-d03a98d44b32, LATTICE_METRICS, LATTICE_METRICS structure [Tablet PC], rectypes/LATTICE_METRICS, tablet.lattice_metrics
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
req.typenames: LATTICE_METRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLATTICE_METRICS
 - rectypes/tagLATTICE_METRICS
 - LATTICE_METRICS
 - rectypes/LATTICE_METRICS
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
 - LATTICE_METRICS
---

# LATTICE_METRICS structure


## -description

Describes the baseline and the midline height.

## -struct-fields

### -field lsBaseline

The <a href="/windows/desktop/api/rectypes/ns-rectypes-line_segment">LINE_SEGMENT</a> structure containing the start and end point of the baseline, in ink coordinates.

### -field iMidlineOffset

Offset of the midline, relative to the baseline, in HIMETRIC units.

## -see-also

<a href="/windows/desktop/api/rectypes/ns-rectypes-line_segment">LINE_SEGMENT Structure</a>