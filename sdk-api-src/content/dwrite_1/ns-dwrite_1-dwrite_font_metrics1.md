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

# DWRITE_FONT_METRICS1 structure


## -description


The <b>DWRITE_FONT_METRICS1</b> structure specifies the metrics that are applicable to all glyphs within the font face.


## -struct-fields




### -field glyphBoxLeft

Left edge of accumulated bounding blackbox of all glyphs in the font.


### -field glyphBoxTop

Top edge of accumulated bounding blackbox of all glyphs in the font.


### -field glyphBoxRight

Right edge of accumulated bounding blackbox of all glyphs in the font.


### -field glyphBoxBottom

Bottom edge of accumulated bounding blackbox of all glyphs in the font.


### -field subscriptPositionX

Horizontal position of the subscript relative to the baseline origin. This is typically negative (to the left) in italic and oblique fonts, and zero in regular fonts.


### -field subscriptPositionY

Vertical position of the subscript relative to the baseline. This is typically negative.


### -field subscriptSizeX

Horizontal size of the subscript em box in design units, used to scale the simulated subscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client uses its own policy.


### -field subscriptSizeY

Vertical size of the subscript em box in design units, used to scale the simulated subscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client uses its own policy.


### -field superscriptPositionX

Horizontal position of the superscript relative to the baseline origin. This is typically positive (to the right) in italic and oblique fonts, and zero in regular fonts.


### -field superscriptPositionY

Vertical position of the superscript relative to the baseline. This is typically positive.


### -field superscriptSizeX

Horizontal size of the superscript em box in design units, used to scale the simulated superscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client should use its own policy.


### -field superscriptSizeY

Vertical size of the superscript em box in design units, used to scale the simulated superscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client should use its own policy.


### -field hasTypographicMetrics

A Boolean value that indicates that the ascent, descent, and lineGap are based on newer 'typographic' values in the font, rather than legacy values.


### -field DWRITE_FONT_METRICS

 




## -remarks



<b>DWRITE_FONT_METRICS1</b> inherits from <a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a>:

<pre class="syntax" xml:space="preserve"><code>
struct DWRITE_FONT_METRICS1 : public DWRITE_FONT_METRICS
{
...
};</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/2D8D22B9-3F5B-4257-8D74-699C4040C9DB">IDWriteFont1::GetMetrics</a>



<a href="https://msdn.microsoft.com/2FD26970-8CF3-453F-A08D-30CC4A820281">IDWriteFontFace1::GetGdiCompatibleMetrics</a>



<a href="https://msdn.microsoft.com/7F899D56-F56B-4C4C-A17D-B42A34CAA0F1">IDWriteFontFace1::GetMetrics</a>
 

 

