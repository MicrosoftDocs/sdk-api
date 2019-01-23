---
UID: NF:gdiplusmatrix.Matrix.Matrix(IN const RectF &,IN const PointF)
title: Matrix::Matrix(IN const RectF &,IN const PointF)
author: windows-sdk-content
description: Creates a Matrix::Matrix object based on a rectangle and a point.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixconstructors\matrix_21rectfamprect_pointfdstplg.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Matrix, Matrix class [GDI+],Matrix constructor, Matrix constructor [GDI+], Matrix constructor [GDI+],Matrix class, Matrix.Matrix, Matrix.Matrix(IN const RectF &,IN const PointF), Matrix.Matrix(const RectF&,const PointF*), Matrix::Matrix, Matrix::Matrix(IN const RectF &,IN const PointF), _gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_, gdiplus._gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_
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
 - Matrix.Matrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::Matrix(IN const RectF &,IN const PointF)


## -description


Creates a <b>Matrix::Matrix</b> object based on a rectangle and a point.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a></b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a> object. The <b>X</b> data member of the rectangle specifies the matrix element in row 1, column 1. The <b>Y</b> data member of the rectangle specifies the matrix element in row 1, column 2. The <b>Width</b> data member of the rectangle specifies the matrix element in row 2, column 1. The <b>Height</b> data member of the rectangle specifies the matrix element in row 2, column 2. 


### -param dstplg [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> object. The <b>X</b> data member of the point specifies the matrix element in row 3, column 1. The <b>Y</b> data member of the point specifies the matrix element in row 3, column 2. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536395(v=VS.85).aspx">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535297(v=VS.85).aspx">Matrix Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

