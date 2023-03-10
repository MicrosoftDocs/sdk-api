---
UID: NS:gdipluscolormatrix.ColorMap
title: ColorMap (gdipluscolormatrix.h)
description: The ColorMap structure contains two Color objects. Several methods of the ImageAttributes class adjust image colors by using a color remap table, which is an array of ColorMap structures.
helpviewer_keywords: ["ColorMap","ColorMap structure [GDI+]","_gdiplus_STRUC_ColorMap","gdiplus._gdiplus_STRUC_ColorMap","gdipluscolormatrix/ColorMap"]
old-location: gdiplus\_gdiplus_STRUC_ColorMap.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colormap.htm
ms.date: 12/05/2018
ms.keywords: ColorMap, ColorMap structure [GDI+], _gdiplus_STRUC_ColorMap, gdiplus._gdiplus_STRUC_ColorMap, gdipluscolormatrix/ColorMap
req.header: gdipluscolormatrix.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ColorMap
 - gdipluscolormatrix/ColorMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluscolormatrix.h
api_name:
 - ColorMap
---

# ColorMap structure


## -description

The <b>ColorMap</b> structure contains two <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects. Several methods of the <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> class adjust image colors by using a color remap table, which is an array of <b>ColorMap</b> structures.

## -struct-fields

### -field oldColor

Type: <b><a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

The original color.

### -field newColor

Type: <b><a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

The new color.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-color-remap-table-use">Using a Color Remap Table</a>