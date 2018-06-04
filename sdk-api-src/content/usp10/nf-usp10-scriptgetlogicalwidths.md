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

# ScriptGetLogicalWidths function


## -description


Converts the glyph <a href="uniscribe_glossary.htm">advance widths</a> for a specific font into logical widths.


## -parameters




### -param psa [in]

Pointer to a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure.


### -param cChars [in]

Count of the logical code points in the run.


### -param cGlyphs [in]

Count of the glyphs in the run.


### -param piGlyphWidth [in]

Pointer to an array of glyph advance widths.


### -param pwLogClust [in]

Pointer to an array of logical clusters.


### -param psva [in]

Pointer to a <a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a> structure defining visual attributes.


### -param piDx [out]

Pointer to an array of logical widths.


## -returns



Currently returns S_OK in all cases.




## -remarks



This function is useful for recording widths in a font-independent manner. It converts the glyph advance widths calculated for a specific font into logical widths, one per code point, in the same order as the code points. If the same string is then displayed on a different device using a different font, the logical widths can be applied by using <a href="https://msdn.microsoft.com/964634f4-700b-47a7-a86f-071f1c97bcbe">ScriptApplyLogicalWidth</a> to approximate the original placement. This mechanism is useful when implementing print preview. On the preview screen, it is important to match the layout and placement of the final printed result.

<div class="alert"><b>Note</b>  Ligature glyph widths are divided evenly among the characters they represent.</div>
<div> </div>
<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a>



<a href="https://msdn.microsoft.com/964634f4-700b-47a7-a86f-071f1c97bcbe">ScriptApplyLogicalWidth</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

