---
UID: NF:gdiplusimageattributes.ImageAttributes.SetBrushRemapTable
title: ImageAttributes::SetBrushRemapTable
author: windows-sdk-content
description: The ImageAttributes::SetBrushRemapTable method sets the color remap table for the brush category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setbrushremaptable.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ImageAttributes class [GDI+],SetBrushRemapTable method, ImageAttributes.SetBrushRemapTable, ImageAttributes::SetBrushRemapTable, SetBrushRemapTable, SetBrushRemapTable method [GDI+], SetBrushRemapTable method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_, gdiplus._gdiplus_CLASS_ImageAttributes_SetBrushRemapTable_mapSize_map_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.SetBrushRemapTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetBrushRemapTable


## -description


The <b>ImageAttributes::SetBrushRemapTable</b> method sets the color remap table for the brush category.


## -parameters




### -param mapSize [in]

Type: <b>UINT</b>

<b>INT</b> that specifies the number of elements in the <i>map</i> array. 


### -param map [in]

Type: <b><a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a> structures. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A color-remap table is an array of <a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a> structures. Each <b>ColorMap</b> structure has two <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> objects: one that specifies an old color and one that specifies a corresponding new color. During rendering, any color that matches one of the old colors in the remap table is changed to the corresponding new color.

Calling the <b>ImageAttributes::SetBrushRemapTable</b> method has the same effect as passing <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeBrush</a> to the <a href="https://msdn.microsoft.com/87b63b0d-9071-4c7f-9ff6-14083092246a">ImageAttributes::SetRemapTable</a> method. The specified remap table applies to items in metafiles that are filled with a brush.


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object and sets its brush remap table so that red is converted to green.


```cpp

ImageAttributes imageAtt;
ColorMap cMap;
cMap.oldColor = Color(255, 255, 0, 0);  // red
cMap.newColor = Color(255, 0, 255, 0);  // green
imageAtt.SetBrushRemapTable(1, &cMap);
				
```





## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

