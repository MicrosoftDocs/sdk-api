---
UID: NF:gdiplusbrush.TextureBrush.TranslateTransform
title: TextureBrush::TranslateTransform (gdiplusbrush.h)
author: windows-sdk-content
description: The TextureBrush::TranslateTransform method updates this brush's current transformation matrix with the product of itself and a translation matrix.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\translatetransform_46dx_dy_order.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TextureBrush class [GDI+],TranslateTransform method, TextureBrush.TranslateTransform, TextureBrush::TranslateTransform, TranslateTransform, TranslateTransform method [GDI+], TranslateTransform method [GDI+],TextureBrush class, _gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_, gdiplus._gdiplus_CLASS_TextureBrush_TranslateTransform_dx_dy_order_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - TextureBrush.TranslateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the 
					<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrderPrepend</a> specifies that the translation matrix is on the left, and <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrderAppend</a> specifies that the translation matrix is on the right. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533858(v=VS.85).aspx">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534526(v=VS.85).aspx">TextureBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534530(v=VS.85).aspx">TextureBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534532(v=VS.85).aspx">TextureBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534534(v=VS.85).aspx">TextureBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534536(v=VS.85).aspx">TextureBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534538(v=VS.85).aspx">TextureBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

