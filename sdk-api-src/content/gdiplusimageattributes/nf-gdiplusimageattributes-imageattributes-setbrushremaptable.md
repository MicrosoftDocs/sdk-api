---
UID: NF:gdiplusimageattributes.ImageAttributes.SetBrushRemapTable
title: ImageAttributes::SetBrushRemapTable (gdiplusimageattributes.h)
description: The ImageAttributes::SetBrushRemapTable method sets the color remap table for the brush category.
helpviewer_keywords: ["ImageAttributes class [GDI+]","SetBrushRemapTable method","ImageAttributes.SetBrushRemapTable","ImageAttributes::SetBrushRemapTable","SetBrushRemapTable","SetBrushRemapTable method [GDI+]","SetBrushRemapTable method [GDI+]","ImageAttributes class","_gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_","gdiplus._gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setbrushremaptable.htm
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],SetBrushRemapTable method, ImageAttributes.SetBrushRemapTable, ImageAttributes::SetBrushRemapTable, SetBrushRemapTable, SetBrushRemapTable method [GDI+], SetBrushRemapTable method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_, gdiplus._gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_
req.header: gdiplusimageattributes.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ImageAttributes::SetBrushRemapTable
 - gdiplusimageattributes/ImageAttributes::SetBrushRemapTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.SetBrushRemapTable
---

# ImageAttributes::SetBrushRemapTable


## -description

The <b>ImageAttributes::SetBrushRemapTable</b> method sets the color remap table for the brush category.

## -parameters

### -param mapSize [in]

Type: <b>UINT</b>

<b>INT</b> that specifies the number of elements in the <i>map</i> array.

### -param map [in]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a> structures.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A color-remap table is an array of <a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a> structures. Each <b>ColorMap</b> structure has two <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects: one that specifies an old color and one that specifies a corresponding new color. During rendering, any color that matches one of the old colors in the remap table is changed to the corresponding new color.

Calling the <b>ImageAttributes::SetBrushRemapTable</b> method has the same effect as passing <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeBrush</a> to the <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable">ImageAttributes::SetRemapTable</a> method. The specified remap table applies to items in metafiles that are filled with a brush.


#### Examples



The following example creates an 
						<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object and sets its brush remap table so that red is converted to green.


```cpp

ImageAttributes imageAtt;
ColorMap cMap;
cMap.oldColor = Color(255, 255, 0, 0);  // red
cMap.newColor = Color(255, 0, 255, 0);  // green
imageAtt.SetBrushRemapTable(1, &cMap);
				
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>