---
UID: NF:usp10.ScriptGetLogicalWidths
title: ScriptGetLogicalWidths function
author: windows-sdk-content
description: Converts the glyph advance widths for a specific font into logical widths.
old-location: intl\scriptgetlogicalwidths.htm
tech.root: Intl
ms.assetid: ecedd0a1-aad8-4527-be46-6f7dd26a9e9b
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ScriptGetLogicalWidths, ScriptGetLogicalWidths function [Internationalization for Windows Applications], _win32_ScriptGetLogicalWidths, intl.scriptgetlogicalwidths, usp10/ScriptGetLogicalWidths
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptGetLogicalWidths
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
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
 

 

