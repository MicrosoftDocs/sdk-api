---
UID: NF:winddi.FONTOBJ_cGetGlyphs
title: FONTOBJ_cGetGlyphs function
author: windows-driver-content
description: The FONTOBJ_cGetGlyphs function is a service to the font consumer that translates glyph handles into pointers to glyph data, which are valid until the next call to FONTOBJ_cGetGlyphs.
old-location: display\fontobj_cgetglyphs.htm
old-project: display
ms.assetid: 0174fc88-e665-427e-b22f-468ddbea5b47
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FONTOBJ_cGetGlyphs, FONTOBJ_cGetGlyphs function [Display Devices], display.fontobj_cgetglyphs, gdifncs_8e402f9d-4ce3-4907-921c-9c0335a3966b.xml, winddi/FONTOBJ_cGetGlyphs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	FONTOBJ_cGetGlyphs
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

