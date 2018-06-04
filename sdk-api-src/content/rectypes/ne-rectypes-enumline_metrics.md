---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

<img alt="Illustration showing components of line metrics" border="" src="images/af81489d-317e-499e-a78b-702519efe530.gif"/>
For East Asian languages written horizontally, the descender line and baseline are located at the bottom of the characters and the ascender line at the top of the characters. The midline is between the ascender and descender lines.

For East Asian languages written vertically, the descender line is the leftmost edge, the ascender line is the rightmost edge, and baseline is between the descender and ascender lines. The midline for Komoji characters is the leftmost edge and the location for punctuation characters depends on the character.



