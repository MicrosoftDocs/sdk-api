---
UID: NE:rectypes.enumLINE_METRICS
title: enumLINE_METRICS
author: windows-sdk-content
description: Represents the lines found in a recognition segment.
old-location: tablet\line_metrics.htm
old-project: tablet
ms.assetid: 1317badb-38e1-41fe-9918-c28da88aa511
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 1317badb-38e1-41fe-9918-c28da88aa511, LINE_METRICS, LINE_METRICS enumeration [Tablet PC], LM_ASCENDER, LM_BASELINE, LM_DESCENDER, LM_MIDLINE, enumLINE_METRICS, rectypes/LINE_METRICS, rectypes/LM_ASCENDER, rectypes/LM_BASELINE, rectypes/LM_DESCENDER, rectypes/LM_MIDLINE, tablet.line_metrics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: LINE_METRICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - LINE_METRICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# enumLINE_METRICS enumeration


## -description



Represents the lines found in a recognition segment.




## -enum-fields




### -field LM_BASELINE

Requests baseline metrics. For an example that shows the baseline of a segment, see the Remarks section.


### -field LM_MIDLINE

Requests midline metrics. For an example that shows the midline of a segment, see the remarks section.


### -field LM_ASCENDER

Requests ascender metrics. For an example that shows the ascender line of a segment, see the Remarks section.


### -field LM_DESCENDER

Requests descender metrics. For an example that shows the decender line of a segment, see the Remarks section.


## -remarks



The following example shows the baseline, midline, ascender line, and descender line of a segment.

<img alt="Illustration showing components of line metrics" border="" src="./images/af81489d-317e-499e-a78b-702519efe530.gif"/>
For East Asian languages written horizontally, the descender line and baseline are located at the bottom of the characters and the ascender line at the top of the characters. The midline is between the ascender and descender lines.

For East Asian languages written vertically, the descender line is the leftmost edge, the ascender line is the rightmost edge, and baseline is between the descender and ascender lines. The midline for Komoji characters is the leftmost edge and the location for punctuation characters depends on the character.



