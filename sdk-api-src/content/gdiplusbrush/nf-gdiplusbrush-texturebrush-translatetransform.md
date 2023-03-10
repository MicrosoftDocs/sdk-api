---
UID: NF:gdiplusbrush.TextureBrush.TranslateTransform
title: TextureBrush::TranslateTransform (gdiplusbrush.h)
description: The TextureBrush::TranslateTransform method updates this brush's current transformation matrix with the product of itself and a translation matrix.
helpviewer_keywords: ["TextureBrush class [GDI+]","TranslateTransform method","TextureBrush.TranslateTransform","TextureBrush::TranslateTransform","TranslateTransform","TranslateTransform method [GDI+]","TranslateTransform method [GDI+]","TextureBrush class","_gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_","gdiplus._gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\translatetransform_46dx_dy_order.htm
ms.date: 12/05/2018
ms.keywords: TextureBrush class [GDI+],TranslateTransform method, TextureBrush.TranslateTransform, TextureBrush::TranslateTransform, TranslateTransform, TranslateTransform method [GDI+], TranslateTransform method [GDI+],TextureBrush class, _gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_, gdiplus._gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_
req.header: gdiplusbrush.h
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
 - TextureBrush::TranslateTransform
 - gdiplusbrush/TextureBrush::TranslateTransform
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
 - TextureBrush.TranslateTransform
---

# TextureBrush::TranslateTransform


## -description

The <b>TextureBrush::TranslateTransform</b> method updates this brush's current transformation matrix with the product of itself and a translation matrix.

## -parameters

### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the horizontal component of the translation.

### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the vertical component of the translation.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the translation matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the translation matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-an-image-texture-use">Filling a Shape with an Image Texture</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-gettransform">TextureBrush::GetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-multiplytransform">TextureBrush::MultiplyTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-resettransform">TextureBrush::ResetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-rotatetransform">TextureBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-scaletransform">TextureBrush::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform">TextureBrush::SetTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>