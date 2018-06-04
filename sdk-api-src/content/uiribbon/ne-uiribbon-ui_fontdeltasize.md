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

# UI_FONTDELTASIZE enumeration


## -description


Specifies values that identify whether the font size of a highlighted text run should be incremented or decremented.


## -enum-fields




### -field UI_FONTDELTASIZE_GROW

Increment the font size.


### -field UI_FONTDELTASIZE_SHRINK

Decrement the font size.


## -remarks



When you highlight a run of heterogeneously sized text, the Ribbon framework sets the <b>Font size</b> control to blank.  When you click the <b>Font grow</b> button or the <b>Font shrink</b> button, the highlighted text is resized, and the relative size variations in the text run are maintained.

The following screen shot shows the <b>Font grow</b> and <b>Font shrink</b> buttons on the <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a>.

<img alt="Screen shot of the Font grow and Font shrink buttons on the FontControl." src="images/Markup/FontControl_IncDec.png"/>




## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/021a6c79-1d3e-47d2-9601-cdaa2e66a50a">UI_PKEY_FontProperties_DeltaSize</a>
 

 

