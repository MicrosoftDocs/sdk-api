---
UID: NS:tpcshrd.tagSTROKE_RANGE
title: STROKE_RANGE (tpcshrd.h)
description: Specifies a range of strokes in the InkDisp object.
helpviewer_keywords: ["STROKE_RANGE","STROKE_RANGE structure [Tablet PC]","cae64877-2ea4-45a1-b5c2-0764c7ebeaf7","tablet.stroke_range","tpcshrd/STROKE_RANGE"]
old-location: tablet\stroke_range.htm
tech.root: tablet
ms.assetid: cae64877-2ea4-45a1-b5c2-0764c7ebeaf7
ms.date: 12/05/2018
ms.keywords: STROKE_RANGE, STROKE_RANGE structure [Tablet PC], cae64877-2ea4-45a1-b5c2-0764c7ebeaf7, tablet.stroke_range, tpcshrd/STROKE_RANGE
req.header: tpcshrd.h
req.include-header: Tcpshrd.h
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
req.typenames: STROKE_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTROKE_RANGE
 - tpcshrd/tagSTROKE_RANGE
 - STROKE_RANGE
 - tpcshrd/STROKE_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - STROKE_RANGE
---

# STROKE_RANGE structure


## -description

Specifies a range of strokes in the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -struct-fields

### -field iStrokeBegin

Index of the first stroke in the range, inclusive.

### -field iStrokeEnd

Index of the last stroke in the range, inclusive.