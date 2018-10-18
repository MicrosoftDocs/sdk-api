---
UID: NF:gdipluspen.Pen.MultiplyTransform
title: Pen::MultiplyTransform
author: windows-sdk-content
description: The Pen::MultiplyTransform method updates the world transformation matrix of this Pen object with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_Pen_MultiplyTransform_matrix_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\multiplytransform_75matrix_order.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],Pen class, Pen class [GDI+],MultiplyTransform method, Pen.MultiplyTransform, Pen::MultiplyTransform, _gdiplus_CLASS_Pen_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_Pen_MultiplyTransform_matrix_order_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspen.h
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
 - Pen.MultiplyTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::MultiplyTransform


## -description


The <b>Pen::MultiplyTransform</b> method updates the world transformation matrix of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object with the product of itself and another matrix.


## -parameters




### -param matrix [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that is multiplied with the world transformation matrix of this 
					<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. <b>MatrixOrderPrepend</b> specifies that the passed matrix is on the left, and <b>MatrixOrderAppend</b> specifies that the passed matrix is on the right. The default value is <b>MatrixOrderPrepend</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536332(v=VS.85).aspx">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535035(v=VS.85).aspx">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535038(v=VS.85).aspx">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535039(v=VS.85).aspx">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535040(v=VS.85).aspx">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535056(v=VS.85).aspx">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

