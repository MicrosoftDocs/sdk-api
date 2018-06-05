---
UID: NF:gdipluspath.GraphicsPath.Widen
title: GraphicsPath::Widen
author: windows-sdk-content
description: The GraphicsPath::Widen method replaces this path with curves that enclose the area that is filled when this path is drawn by a specified pen. The GraphicsPath::Widen method also flattens the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Widen_pen_matrix_flatness_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\widen.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GraphicsPath class [GDI+],Widen method, GraphicsPath.Widen, GraphicsPath::Widen, Widen, Widen method [GDI+], Widen method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Widen_pen_matrix_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Widen_pen_matrix_flatness_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	GraphicsPath.Widen
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPath::Widen


## -description


The <b>GraphicsPath::Widen</b> method replaces this path with curves that enclose the area that is filled when this path is drawn by a specified pen. The <b>GraphicsPath::Widen</b> method also flattens the path.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. The path is made as wide as it would be when drawn by this pen. 


### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies a transformation to be applied along with the widening. If this parameter is <b>NULL</b>, no transformation is applied. The default value is <b>NULL</b>. 


### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that specifies the maximum error between the path and its flattened approximation. Reducing the flatness increases the number of line segments in the approximation. The default value is FlatnessDefault, which is a constant defined in Gdiplusenums.h. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8">Flattening Paths</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/947b3e68-67ad-47fb-80bb-b5a678f71381">GraphicsPath::Flatten</a>



<a href="https://msdn.microsoft.com/f896fcfd-2094-46f0-a9f8-469f13dccfa2">GraphicsPath::Outline</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>
 

 

