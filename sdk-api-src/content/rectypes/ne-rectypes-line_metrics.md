---
UID: NE:rectypes.enumLINE_METRICS
title: LINE_METRICS (rectypes.h)
description: Represents the lines found in a recognition segment.
helpviewer_keywords: ["1317badb-38e1-41fe-9918-c28da88aa511","LINE_METRICS","LINE_METRICS enumeration [Tablet PC]","LM_ASCENDER","LM_BASELINE","LM_DESCENDER","LM_MIDLINE","rectypes/LINE_METRICS","rectypes/LM_ASCENDER","rectypes/LM_BASELINE","rectypes/LM_DESCENDER","rectypes/LM_MIDLINE","tablet.line_metrics"]
old-location: tablet\line_metrics.htm
tech.root: tablet
ms.assetid: 1317badb-38e1-41fe-9918-c28da88aa511
ms.date: 12/05/2018
ms.keywords: 1317badb-38e1-41fe-9918-c28da88aa511, LINE_METRICS, LINE_METRICS enumeration [Tablet PC], LM_ASCENDER, LM_BASELINE, LM_DESCENDER, LM_MIDLINE, rectypes/LINE_METRICS, rectypes/LM_ASCENDER, rectypes/LM_BASELINE, rectypes/LM_DESCENDER, rectypes/LM_MIDLINE, tablet.line_metrics
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
req.typenames: LINE_METRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - enumLINE_METRICS
 - rectypes/enumLINE_METRICS
 - LINE_METRICS
 - rectypes/LINE_METRICS
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
 - LINE_METRICS
---

# LINE_METRICS enumeration


## -description

Represents the lines found in a recognition segment.

## -enum-fields

### -field LM_BASELINE:0

Requests baseline metrics. For an example that shows the baseline of a segment, see the Remarks section.

### -field LM_MIDLINE:1

Requests midline metrics. For an example that shows the midline of a segment, see the remarks section.

### -field LM_ASCENDER:2

Requests ascender metrics. For an example that shows the ascender line of a segment, see the Remarks section.

### -field LM_DESCENDER:3

Requests descender metrics. For an example that shows the descender line of a segment, see the Remarks section.

## -remarks

The following example shows the baseline, midline, ascender line, and descender line of a segment.

<img alt="Illustration showing components of line metrics" border="" src="images/af81489d-317e-499e-a78b-702519efe530.gif"/>
For East Asian languages written horizontally, the descender line and baseline are located at the bottom of the characters and the ascender line at the top of the characters. The midline is between the ascender and descender lines.

For East Asian languages written vertically, the descender line is the leftmost edge, the ascender line is the rightmost edge, and baseline is between the descender and ascender lines. The midline for Komoji characters is the leftmost edge and the location for punctuation characters depends on the character.

