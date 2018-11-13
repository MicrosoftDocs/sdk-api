---
UID: NF:gdipluspath.GraphicsPath.Widen
title: GraphicsPath::Widen
author: windows-sdk-content
description: The GraphicsPath::Widen method replaces this path with curves that enclose the area that is filled when this path is drawn by a specified pen. The GraphicsPath::Widen method also flattens the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Widen_pen_matrix_flatness_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\widen.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GraphicsPath class [GDI+],Widen method, GraphicsPath.Widen, GraphicsPath::Widen, Widen, Widen method [GDI+], Widen method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Widen_pen_matrix_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Widen_pen_matrix_flatness_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
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
 - GraphicsPath.Widen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::Widen


## -description


The <b>GraphicsPath::Widen</b> method replaces this path with curves that enclose the area that is filled when this path is drawn by a specified pen. The <b>GraphicsPath::Widen</b> method also flattens the path.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object. The path is made as wide as it would be when drawn by this pen. 


### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that specifies a transformation to be applied along with the widening. If this parameter is <b>NULL</b>, no transformation is applied. The default value is <b>NULL</b>. 


### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that specifies the maximum error between the path and its flattened approximation. Reducing the flatness increases the number of line segments in the approximation. The default value is FlatnessDefault, which is a constant defined in Gdiplusenums.h. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536364(v=VS.85).aspx">Flattening Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535530(v=VS.85).aspx">GraphicsPath::Flatten</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535564(v=VS.85).aspx">GraphicsPath::Outline</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>
 

 

