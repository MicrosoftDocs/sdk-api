---
UID: NF:gdiplusgraphics.Graphics.RotateTransform
title: Graphics::RotateTransform
author: windows-sdk-content
description: The Graphics::RotateTransform method updates the world transformation matrix of this Graphics object with the product of itself and a rotation matrix.
old-location: gdiplus\_gdiplus_CLASS_Graphics_RotateTransform_angle_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\rotatetransform.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Graphics class [GDI+],RotateTransform method, Graphics.RotateTransform, Graphics::RotateTransform, RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_Graphics_RotateTransform_angle_order_
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
 - Graphics.RotateTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::RotateTransform


## -description


The <b>Graphics::RotateTransform</b> method updates the world transformation matrix of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object with the product of itself and a rotation matrix.


## -parameters




### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, of rotation. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of multiplication. MatrixOrderPrepend specifies that the rotation matrix is on the left, and MatrixOrderAppend specifies that the rotation matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536332(v=VS.85).aspx">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535729(v=VS.85).aspx">Graphics::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535800(v=VS.85).aspx">Graphics::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535803(v=VS.85).aspx">Graphics::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535807(v=VS.85).aspx">Graphics::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535818(v=VS.85).aspx">Graphics::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535819(v=VS.85).aspx">Graphics::TransformPoints</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535820(v=VS.85).aspx">Graphics::TranslateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

