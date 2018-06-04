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

# D2D1_PRINT_FONT_SUBSET_MODE enumeration


## -description


Defines when font resources should be subset during printing.


## -enum-fields




### -field D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT


### -field D2D1_PRINT_FONT_SUBSET_MODE_EACHPAGE


### -field D2D1_PRINT_FONT_SUBSET_MODE_NONE


### -field D2D1_PRINT_FONT_SUBSET_MODE_FORCE_DWORD




#### - D2D1_PRINT_FONT_SUBSET_DEFAULT

Uses a heuristic strategy to decide when to subset fonts. 

<div class="alert"><b>Note</b>  If the print driver has requested archive-optimized content, then Direct2D will subset fonts once, for the entire document.</div>
<div> </div>

#### - D2D1_PRINT_FONT_SUBSET_EACHPAGE

Subsets and embeds font resources in each page, then discards that font subset after the page is printed out. 


#### - D2D1_PRINT_FONT_SUBSET_NONE

Sends out the original font resources without subsetting along with the page that first uses the font, and re-uses the font resources for later pages without resending them.  


## -see-also




<a href="https://msdn.microsoft.com/5A4D4DDC-4161-44A2-9EB6-E4C14696B810">D2D1_PRINT_CONTROL_PROPERTIES</a>
 

 

