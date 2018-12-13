---
UID: NF:gdiplusmatrix.Matrix.Shear
title: Matrix::Shear
author: windows-sdk-content
description: The Matrix::Shear method updates this matrix with the product of itself and a shearing matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\shear.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Matrix class [GDI+],Shear method, Matrix.Shear, Matrix::Shear, Shear, Shear method [GDI+], Shear method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_, gdiplus._gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusmatrix.h
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
 - Matrix.Shear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::Shear


## -description


The <b>Matrix::Shear</b> method updates this matrix with the product of itself and a shearing matrix.


## -parameters




### -param shearX [in]

Type: <b>REAL</b>

Real number that specifies the horizontal shear factor. 


### -param shearY [in]

Type: <b>REAL</b>

Real number that specifies the vertical shear factor. 


### -param order [in]

Type: <b>REAL</b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the shearing matrix is on the left, and MatrixOrderAppend specifies that the shearing matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the Status enumeration.




## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/4dcf4a79-87b7-4496-907c-5a6549f1502d">Matrix::Multiply</a>



<a href="https://msdn.microsoft.com/ddbc7a4a-61aa-4daf-82ab-f1347f41f58b">Matrix::Rotate</a>



<a href="https://msdn.microsoft.com/49350cae-15f0-40ff-9655-c35432faa0ef">Matrix::RotateAt</a>



<a href="https://msdn.microsoft.com/a68cfed2-25a0-45de-83db-5f518587469a">Matrix::Scale</a>



<a href="https://msdn.microsoft.com/c4ac476f-ee9d-439b-8686-3edfea64ec39">Matrix::Translate</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

