---
UID: NS:gdipluscolormatrix.ColorMatrix
title: ColorMatrix
author: windows-sdk-content
description: The ColorMatrix structure contains a 5&#215;5 matrix of real numbers. Several methods of the ImageAttributes class adjust image colors by using a color matrix.
old-location: gdiplus\_gdiplus_STRUC_ColorMatrix.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colormatrix.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ColorMatrix, ColorMatrix structure [GDI+], _gdiplus_STRUC_ColorMatrix, gdiplus._gdiplus_STRUC_ColorMatrix, gdipluscolormatrix/ColorMatrix
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluscolormatrix.h
api_name:
 - ColorMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ColorMatrix structure


## -description


The <b>ColorMatrix</b> structure contains a 5×5 matrix of real numbers. Several methods of the <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> class adjust image colors by using a color matrix.


## -struct-fields




### -field m

Type: <b>REAL[5]</b>

5×5 array of real numbers. 


## -remarks



A 5×5 color matrix is a homogeneous matrix for a 4-space transformation. The element in the fifth row and fifth column of a 5×5 homogeneous matrix must be 1, and all of the other elements in the fifth column must be 0. Color matrices are used to transform color vectors. The first four components of a color vector hold the red, green, blue, and alpha components (in that order) of a color. The fifth component of a color vector is always 1.




## -see-also




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

