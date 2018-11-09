---
UID: NS:winddi._FD_GLYPHATTR
title: "_FD_GLYPHATTR"
author: windows-sdk-content
description: The FD_GLYPHATTR structure is used to specify the return value for the FONTOBJ_pQueryGlyphAttrs and DrvQueryGlyphAttrs functions.
old-location: display\fd_glyphattr.htm
tech.root: display
ms.assetid: 25a5c390-244c-4cff-a6a5-cc61fc5aa40b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PFD_GLYPHATTR, FD_GLYPHATTR, FD_GLYPHATTR structure [Display Devices], PFD_GLYPHATTR, PFD_GLYPHATTR structure pointer [Display Devices], _FD_GLYPHATTR, display.fd_glyphattr, grstrcts_5edf5620-9123-4fdd-b402-d7e06bdeee2a.xml, winddi/FD_GLYPHATTR, winddi/PFD_GLYPHATTR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - FD_GLYPHATTR
product: Windows
targetos: Windows
req.typenames: FD_GLYPHATTR, *PFD_GLYPHATTR
req.redist: 
---

# _FD_GLYPHATTR structure


## -description


The FD_GLYPHATTR structure is used to specify the return value for the <a href="https://msdn.microsoft.com/6a619922-5ab6-4169-8b41-e645e9d7fe93">FONTOBJ_pQueryGlyphAttrs</a> and <a href="https://msdn.microsoft.com/cfc42384-581c-4358-84a9-91028c89bbd8">DrvQueryGlyphAttrs</a> functions.


## -struct-fields




### -field cjThis

Is the size in bytes of the FD_GLYPHATTR structure, including the array specified by the <b>aGlyphAttr</b> member.


### -field cGlyphs

Specifies the number of glyphs in the font.


### -field iMode

Is a flag indicating the type of information being returned. The following flag is defined:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
FO_ATTR_MODE_ROTATE

</td>
<td>
The array specified by <b>aGlyphAttr</b> is a bit array indicating which glyphs of a vertical font must be rotated. The bit array's length is (<b>cGlyphs</b>+7)/8. If a glyph's bit is set, the glyph should be rotated during rasterization.

</td>
</tr>
</table>
 


### -field aGlyphAttr

Is an array supplying the information specified by <b>iMode</b>. The size of this array is (<b>cGlyphs</b>+7) / 8 bytes.


## -remarks



If <b>iMode</b> is FO_ATTR_MODE_ROTATE (the only flag currently defined), a printer driver can determine the bit that corresponds to a particular glyph index using the following code fragment, where <i>hg</i> is the glyph index and <i>pga</i> is a pointer to an FD_GLYPHATTR structure. If the bit in the <b>aGlyphAttr</b> array associated with glyph index <i>hg</i> is set, <i>result</i> is set to 1. If the same bit in the array is not set, <i>result</i> is set to 0. Note that the bits within a byte are stored so that glyph indexes 0, 1, ..., 7 correspond to bit positions 7, 6, ..., 0 within <b>aGlyphAttr</b>[0], glyph indexes 8, 9, ..., 15 correspond to bit positions 7, 6, ..., 0 within <b>aGlyphAttr</b>[1], and so on. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>BYTE glyphBits[8] = {0x80, 0x40, 0x20, 0x10, 0x8, 0x4, 0x2, 0x1};
result = (pga-&gt;aGlyphAttr[hg / 8]) &amp; (glyphBits[hg % 8]);</pre>
</td>
</tr>
</table></span></div>


