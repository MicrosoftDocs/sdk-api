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

# FONTOBJ_cGetGlyphs function


## -description


The <b>FONTOBJ_cGetGlyphs</b> function is a service to the font consumer that translates glyph handles into pointers to glyph data, which are valid until the next call to <b>FONTOBJ_cGetGlyphs</b>. 


## -parameters




### -param pfo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure containing the glyph handles to be translated.


### -param iMode [in]

Specifies whether data will be written as bitmaps or as outline objects. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FO_GLYPHBITS

</td>
<td>
Data will consist of <a href="https://msdn.microsoft.com/library/windows/hardware/ff566818">GLYPHBITS</a> structures that define the bitmaps of the glyphs.

</td>
</tr>
<tr>
<td>
FO_PATHOBJ

</td>
<td>
Data will consist of <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structures that define the outlines of the glyphs.

To determine whether the path should be filled or stroked, the font consumer should check the <b>flInfo</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure. If the FM_INFO_RETURNS_STROKES flag is set, the path should be stroked; otherwise, the path should be filled.

</td>
</tr>
</table>
 


### -param cGlyph

Specifies the number of glyphs to be translated. The only acceptable value is 1 (the code assumes 1, regardless of the value specified).


### -param phg

Pointer to an array of <i>cGlyph</i> HGLYPH structures supplied by the driver.


### -param ppvGlyph

Pointer to a memory location that receives the address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff566819">GLYPHDATA</a> structure. The first member of this structure is a <a href="https://msdn.microsoft.com/library/windows/hardware/ff566822">GLYPHDEF</a> union, which contains a pointer to either a GLYPHBITS structure or a PATHOBJ structure, depending on the value of the <i>iMode</i> parameter. If the value of <i>iMode</i> is FO_GLYPHBITS, (*<i>ppvGlyph)</i>-&gt;<i>gdf</i> contains the address of a GLYPHBITS structure. If the value of <i>iMode</i> is FO_PATHOBJ, (*<i>ppvGlyph</i>)-&gt;<i>gdf</i> contains the address of a PATHOBJ structure. 


## -returns



The return value is the count of pointers passed to the driver if the function is successful. Otherwise, it is zero, and an error code is logged.




## -remarks



This function should be used if the driver is caching fonts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556230">DrvGetGlyphMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565977">FONTOBJ_cGetAllGlyphHandles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566818">GLYPHBITS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>
 

 

