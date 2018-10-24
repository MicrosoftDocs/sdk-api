---
UID: NS:winddi._FD_DEVICEMETRICS
title: "_FD_DEVICEMETRICS"
author: windows-sdk-content
description: The FD_DEVICEMETRICS structure is used to provide device-specific font information to GDI if the iMode parameter of the driver-supplied DrvQueryFontData function is QFD_MAXEXTENTS.
old-location: display\fd_devicemetrics.htm
tech.root: display
ms.assetid: c6518325-7efc-46dd-831b-7cb7d2f37ddb
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PFD_DEVICEMETRICS, FD_DEVICEMETRICS, FD_DEVICEMETRICS structure [Display Devices], PFD_DEVICEMETRICS, PFD_DEVICEMETRICS structure pointer [Display Devices], _FD_DEVICEMETRICS, display.fd_devicemetrics, grstrcts_56d66436-e791-4e40-8764-8a15ae4b6853.xml, winddi/FD_DEVICEMETRICS, winddi/PFD_DEVICEMETRICS"
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
 - FD_DEVICEMETRICS
product: Windows
targetos: Windows
req.typenames: FD_DEVICEMETRICS, *PFD_DEVICEMETRICS
req.redist: 
---

# _FD_DEVICEMETRICS structure


## -description


The FD_DEVICEMETRICS structure is used to provide device-specific font information to GDI if the <i>iMode</i> parameter of the driver-supplied <a href="https://msdn.microsoft.com/3f6efd3c-3ddf-4ce6-9527-730e01c45e74">DrvQueryFontData</a> function is QFD_MAXEXTENTS.


## -struct-fields




### -field flRealizedType

Is a set of accelerator flags. This value can be a combination of the following values:





#### FDM_TYPE_BM_SIDE_CONST

An accelerator for horizontal and vertical writing. If this flag is set, the font has constant height for all bitmaps. In the horizontal case, this means that the <i>cy</i> dimension is constant; in the vertical case, this means that the <i>cx</i> dimension is constant. This accelerator is not used for outlines.





#### FDM_TYPE_CHAR_INC_EQUAL_BM_BASE

An accelerator for horizontal and vertical writing. In the horizontal case, if this flag is set, each glyph's advance width is equal to the <i>cx</i> dimension of the glyph bitmap; in the vertical case, if this flag is set, each glyph's advance width is equal to the <i>cy</i> dimension of the glyph bitmap. This accelerator is not used for outlines.





#### FDM_TYPE_CONST_BEARINGS

If set, the a and c spacing is constant for all glyphs.





#### FDM_TYPE_MAXEXT_EQUAL_BM_SIDE

This flag can be set only if FDM_TYPE_BM_SIDE_CONST is also set. If set, the font height (as defined above for horizontal and vertical writing) is equal to the sum of max ascender and max descender. This accelerator is not used for outlines.





#### FDM_TYPE_ZERO_BEARINGS

If set, the a and c spacing is zero for all glyphs.


### -field pteBase

Specifies a POINTE structure that contains the notional space unit vector along the font's baseline, transformed to device space and then normalized. For more information, see POINTE in <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -field pteSide

Specifies POINTE structure that contains a notional space unit vector perpendicular to the font's baseline in the direction of the ascender, transformed to device space and then normalized. In notional space, baseline and ascender directions must be orthogonal, but in device space, <b>pteBase</b> and <b>pteSide</b> do not have to be orthogonal, depending on the Notional to Device space transform.


### -field lD

Specifies the advance width if the font is a fixed pitch (monospaced) font. If the font is a variable pitch font, this member should be set to zero.


### -field fxMaxAscender

Specifies the hinted maximum ascender height for this font instance, measured along <b>pteSide</b>. See the FIX data type in <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -field fxMaxDescender

Specifies the hinted maximum descender height for this font instance, measured along <b>pteSide</b>. See the FIX data type in <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -field ptlUnderline1

Specifies a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that contains the hinted underline position for this font instance, relative to the glyph's character origin.


### -field ptlStrikeOut

Specifies a POINTL structure that contains the hinted strikeout position for this font instance, relative to the glyph's character origin.


### -field ptlULThickness

Specifies a POINTL structure that contains the hinted underline thickness for this font instance. This vector defines the side of the rectangle used to draw the underline. The base is implicitly defined by the baseline.


### -field ptlSOThickness

Specifies a POINTL structure that contains the hinted strikeout thickness for this font instance. This vector defines the side of the rectangle used to draw the strikeout. The base is implicitly defined by the baseline.


### -field cxMax

Specifies the hinted maximum glyph bitmap width, in pixels, for this font instance. Not used for outlines.


### -field cyMax

Specifies the hinted maximum glyph bitmap height, in pixels, for this font instance. Not used for outlines.


### -field cjGlyphMax

Specifies the hinted maximum size of a glyph, in bytes, for this font instance. This value is the maximum size of the <a href="https://msdn.microsoft.com/d7e0b5dd-dd94-4fc2-8c90-0d656a84c46b">GLYPHBITS</a> structure needed to store any of the font's glyphs.


### -field fdxQuantized

Specifies an <a href="https://msdn.microsoft.com/4d15a771-fbf2-46ed-9698-faa3840f5f76">FD_XFORM</a> structure. The font driver fills in the font transformation that is actually used in the realization of the font. This may differ from the transformation requested by GDI as defined by <a href="https://msdn.microsoft.com/94d8ddf6-221f-47f0-8772-4364ad2ac1a2">FONTOBJ_pxoGetXform</a>.


### -field lNonLinearExtLeading

Is the nonlinear external leading in 28.4 device units.


### -field lNonLinearIntLeading

Is the nonlinear internal leading in 28.4 device units.


### -field lNonLinearMaxCharWidth

Is the nonlinear maximum character increment in 28.4 device units.


### -field lNonLinearAvgCharWidth

Is the nonlinear average character width in 28.4 device units.


### -field lMinA

Is the largest negative A space for this font realization, specified as an absolute value.


### -field lMinC

Is the largest negative C space for this font realization, specified as an absolute value.


### -field lMinD

Is the smallest nonzero character width for this font realization.


### -field alReserved

Is reserved and should be ignored by the font provider.


## -see-also




<a href="https://msdn.microsoft.com/3f6efd3c-3ddf-4ce6-9527-730e01c45e74">DrvQueryFontData</a>



<a href="https://msdn.microsoft.com/4d15a771-fbf2-46ed-9698-faa3840f5f76">FD_XFORM</a>



<a href="https://msdn.microsoft.com/94d8ddf6-221f-47f0-8772-4364ad2ac1a2">FONTOBJ_pxoGetXform</a>



<a href="https://msdn.microsoft.com/d7e0b5dd-dd94-4fc2-8c90-0d656a84c46b">GLYPHBITS</a>
 

 

