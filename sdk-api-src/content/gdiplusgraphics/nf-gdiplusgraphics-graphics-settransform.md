---
UID: NF:gdiplusgraphics.Graphics.SetTransform
title: Graphics::SetTransform
author: windows-sdk-content
description: The Graphics::SetTransform method sets the world transformation of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetTransform_matrix_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\settransform.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Graphics class [GDI+],SetTransform method, Graphics.SetTransform, Graphics::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetTransform_matrix_, gdiplus._gdiplus_CLASS_Graphics_SetTransform_matrix_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusgraphics.h
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.SetTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::SetTransform


## -description


The <b>Graphics::SetTransform</b> method sets the world transformation of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a> object that specifies the world transformation. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/ms536332(v=VS.85).aspx">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/library/ms535729(v=VS.85).aspx">Graphics::GetTransform</a>



<a href="https://msdn.microsoft.com/library/ms535800(v=VS.85).aspx">Graphics::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/library/ms535803(v=VS.85).aspx">Graphics::ResetTransform</a>



<a href="https://msdn.microsoft.com/library/ms535805(v=VS.85).aspx">Graphics::RotateTransform</a>



<a href="https://msdn.microsoft.com/library/ms535807(v=VS.85).aspx">Graphics::ScaleTransform</a>



<a href="https://msdn.microsoft.com/library/ms535819(v=VS.85).aspx">Graphics::TransformPoints</a>



<a href="https://msdn.microsoft.com/library/ms535820(v=VS.85).aspx">Graphics::TranslateTransform</a>



<a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

