---
UID: NS:gdipluscolormatrix.ColorMap
title: ColorMap
author: windows-sdk-content
description: The ColorMap structure contains two Color objects. Several methods of the ImageAttributes class adjust image colors by using a color remap table, which is an array of ColorMap structures.
old-location: gdiplus\_gdiplus_STRUC_ColorMap.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colormap.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ColorMap, ColorMap structure [GDI+], _gdiplus_STRUC_ColorMap, gdiplus._gdiplus_STRUC_ColorMap, gdipluscolormatrix/ColorMap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdipluscolormatrix.h
api_name:
-	ColorMap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# ColorMap structure


## -description


The <b>ColorMap</b> structure contains two <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> objects. Several methods of the <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> class adjust image colors by using a color remap table, which is an array of <b>ColorMap</b> structures.


## -struct-fields




### -field oldColor

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

The original color. 


### -field newColor

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

The new color. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122">Using a Color Remap Table</a>
 

 

