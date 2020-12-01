---
UID: NF:gdiplusgraphics.Graphics.RotateTransform
title: Graphics::RotateTransform (gdiplusgraphics.h)
description: The Graphics::RotateTransform method updates the world transformation matrix of this Graphics object with the product of itself and a rotation matrix.
helpviewer_keywords: ["Graphics class [GDI+]","RotateTransform method","Graphics.RotateTransform","Graphics::RotateTransform","RotateTransform","RotateTransform method [GDI+]","RotateTransform method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_RotateTransform_angle_order_","gdiplus._gdiplus_CLASS_Graphics_RotateTransform_angle_order_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_RotateTransform_angle_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\rotatetransform.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],RotateTransform method, Graphics.RotateTransform, Graphics::RotateTransform, RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_Graphics_RotateTransform_angle_order_
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::RotateTransform
 - gdiplusgraphics/Graphics::RotateTransform
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
 - Graphics.RotateTransform
---

# Graphics::RotateTransform


## -description

The <b>Graphics::RotateTransform</b> method updates the world transformation matrix of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object with the product of itself and a rotation matrix.

## -parameters

### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, of rotation.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of multiplication. MatrixOrderPrepend specifies that the rotation matrix is on the left, and MatrixOrderAppend specifies that the rotation matrix is on the right. The default value is MatrixOrderPrepend.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gettransform">Graphics::GetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform">Graphics::MultiplyTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-resettransform">Graphics::ResetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform">Graphics::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform">Graphics::SetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-transformpoints(incoordinatespace_incoordinatespace_inoutpoint_inint)">Graphics::TransformPoints</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform">Graphics::TranslateTransform</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>