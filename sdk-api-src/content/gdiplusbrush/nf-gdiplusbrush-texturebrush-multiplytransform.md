---
UID: NF:gdiplusbrush.TextureBrush.MultiplyTransform
title: TextureBrush::MultiplyTransform (gdiplusbrush.h)
description: The TextureBrush::MultiplyTransform method updates this brush's transformation matrix with the product of itself and another matrix.
helpviewer_keywords: ["MultiplyTransform","MultiplyTransform method [GDI+]","MultiplyTransform method [GDI+]","TextureBrush class","TextureBrush class [GDI+]","MultiplyTransform method","TextureBrush.MultiplyTransform","TextureBrush::MultiplyTransform","_gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_","gdiplus._gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\multiplytransform_37matrix_order.htm
ms.date: 12/05/2018
ms.keywords: MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],MultiplyTransform method, TextureBrush.MultiplyTransform, TextureBrush::MultiplyTransform, _gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_
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
 - TextureBrush::MultiplyTransform
 - gdiplusbrush/TextureBrush::MultiplyTransform
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
 - TextureBrush.MultiplyTransform
---

# TextureBrush::MultiplyTransform


## -description

The <b>TextureBrush::MultiplyTransform</b> method updates this brush's transformation matrix with the product of itself and another matrix.

## -parameters

### -param matrix [in]

Type: <b><a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to the matrix to be multiplied by this brush's current transformation matrix.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the passed matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the passed matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

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



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-resettransform">TextureBrush::ResetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-rotatetransform">TextureBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-scaletransform">TextureBrush::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform">TextureBrush::SetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-translatetransform">TextureBrush::TranslateTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>