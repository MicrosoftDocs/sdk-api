---
UID: NF:d2d1helper.Matrix3x2F.Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)
title: Matrix3x2F::Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT) (d2d1helper.h)
description: Instantiates a new instance of the Matrix3x2F class that contains the specified values.
helpviewer_keywords: ["D2D1.Matrix3x2F.Matrix3x2F","D2D1::Matrix3x2F::Matrix3x2F","Matrix3x2F","Matrix3x2F constructor [Direct2D]","Matrix3x2F constructor [Direct2D]","Matrix3x2F interface","Matrix3x2F interface [Direct2D]","Matrix3x2F constructor","Matrix3x2F.Matrix3x2F","Matrix3x2F.Matrix3x2F(FLOAT","FLOAT","FLOAT","FLOAT","FLOAT","FLOAT)","Matrix3x2F::Matrix3x2F","Matrix3x2F::Matrix3x2F(FLOAT","FLOAT","FLOAT","FLOAT","FLOAT","FLOAT)","d2d1helper/Matrix3x2F::Matrix3x2F","direct2d.matrix3x2f_matrix3x2f_float__float__float__float__float__float_"]
old-location: direct2d\matrix3x2f_matrix3x2f_float__float__float__float__float__float_.htm
tech.root: Direct2D
ms.assetid: f4701597-9473-4333-9e6d-60000ccea40e
ms.date: 12/05/2018
ms.keywords: D2D1.Matrix3x2F.Matrix3x2F, D2D1::Matrix3x2F::Matrix3x2F, Matrix3x2F, Matrix3x2F constructor [Direct2D], Matrix3x2F constructor [Direct2D],Matrix3x2F interface, Matrix3x2F interface [Direct2D],Matrix3x2F constructor, Matrix3x2F.Matrix3x2F, Matrix3x2F.Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT), Matrix3x2F::Matrix3x2F, Matrix3x2F::Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT), d2d1helper/Matrix3x2F::Matrix3x2F, direct2d.matrix3x2f_matrix3x2f_float__float__float__float__float__float_
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: D2D1
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Matrix3x2F::Matrix3x2F
 - d2d1helper/Matrix3x2F::Matrix3x2F
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - Matrix3x2F.Matrix3x2F
---

# Matrix3x2F::Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)


## -description

Instantiates a new instance of the <a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f">Matrix3x2F</a> class that contains the specified values.

## -parameters

### -param m11

Type: <b>FLOAT</b>

The value in the first row and first column of the matrix.

### -param m12

Type: <b>FLOAT</b>

The value in the first row and second column of the matrix.

### -param m21

Type: <b>FLOAT</b>

The value in the second row and first column of the matrix.

### -param m22

Type: <b>FLOAT</b>

The value in the second row and second column of the matrix.

### -param m31

Type: <b>FLOAT</b>

The value in the third row and first column of the matrix.

### -param m32

Type: <b>FLOAT</b>

The value in the third row and second column of the matrix.

## -remarks

This method enables you to explicitly set the values of  matrix members. When using this method, ensure that each member represents an appropriate value for your transformation matrix. For example, to create the identity matrix, you must set <i>_11</i> and <i>_22</i> to 1, and the rest to 0. To create a translation matrix, you must set <i>_11</i> and <i>_22</i> to 1, <i>_12</i> and <i>_21</i> to 0, <i>_31</i> to the x displacement, and <i>_32</i> to the y displacement.

For convenience and accuracy, we recommended that whenever possible you use other helper functions, such as <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-identity">Identity</a> and <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)">Translation</a>, instead of this one.

## -see-also

<a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f">Matrix3x2F</a>