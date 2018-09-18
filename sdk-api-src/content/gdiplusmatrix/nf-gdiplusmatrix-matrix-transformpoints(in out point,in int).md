---
UID: NF:gdiplusmatrix.Matrix.TransformPoints(IN OUT Point,IN INT)
title: Matrix::TransformPoints(IN OUT Point,IN INT)
author: windows-sdk-content
description: The Matrix::TransformPoints method multiplies each point in an array by this matrix. Each point is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.
old-location: gdiplus\_gdiplus_CLASS_Matrix_TransformPoints_PointF_pts_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\matrixtransformpointsmethods\transformpoints_81pointfpts_intcount.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Matrix class [GDI+],TransformPoints method, Matrix.TransformPoints, Matrix.TransformPoints(IN OUT Point,IN INT), Matrix.TransformPoints(PointF*,INT), Matrix::TransformPoints, Matrix::TransformPoints(IN OUT Point,IN INT), TransformPoints, TransformPoints method [GDI+], TransformPoints method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_TransformPoints_PointF_pts_INT_count_, gdiplus._gdiplus_CLASS_Matrix_TransformPoints_PointF_pts_INT_count_
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

Type: <b><a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> objects that, on input, contains the points to be transformed and, on output, receives the transformed points. Each point in the array is transformed (multiplied by this matrix) and updated with the result of the transformation. 


### -param count [in]

Type: <b>INT</b>

Optional. Integer that specifies the number of points to be transformed. The default value is 1. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>



<a href="https://msdn.microsoft.com/a290aa79-64a0-440e-bfec-a8e66057ec14">TransformPoints Methods</a>



<a href="https://msdn.microsoft.com/6a2ed6a7-825a-422b-b035-b88746f3ab5d">TransformVectors Methods</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

