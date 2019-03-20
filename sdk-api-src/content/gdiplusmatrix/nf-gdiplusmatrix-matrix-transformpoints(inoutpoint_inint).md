---
UID: NF:gdiplusmatrix.Matrix.TransformPoints(IN OUT Point,IN INT)
title: Matrix::TransformPoints(IN OUT Point,IN INT) (gdiplusmatrix.h)
author: windows-sdk-content
description: The Matrix::TransformPoints method multiplies each point in an array by this matrix. Each point is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.
old-location: gdiplus\_gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\matrixtransformpointsmethods\transformpoints_78pointpts_intcount.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Matrix class [GDI+],TransformPoints method, Matrix.TransformPoints, Matrix.TransformPoints(IN OUT Point,IN INT), Matrix.TransformPoints(Point*,INT), Matrix::TransformPoints, Matrix::TransformPoints(IN OUT Point,IN INT), TransformPoints, TransformPoints method [GDI+], TransformPoints method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_, gdiplus._gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_
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
 - Matrix.TransformPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::TransformPoints(IN OUT Point,IN INT)


## -description


The <b>Matrix::TransformPoints</b> method multiplies each point in an array by this matrix. Each point is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.


## -parameters




### -param pts [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a> objects that, on input, contains the points to be transformed and, on output, receives the transformed points. Each point in the array is transformed (multiplied by this matrix) and updated with the result of the transformation. 


### -param count [in]

Type: <b>INT</b>

Optional. Integer that specifies the number of points to be transformed. The default value is 1. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536395(v=VS.85).aspx">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535306(v=VS.85).aspx">TransformPoints Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535307(v=VS.85).aspx">TransformVectors Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

