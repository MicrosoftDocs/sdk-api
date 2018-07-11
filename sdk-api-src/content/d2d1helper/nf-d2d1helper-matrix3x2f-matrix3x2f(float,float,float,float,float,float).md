---
UID: NF:d2d1helper.Matrix3x2F.Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)
title: Matrix3x2F::Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)
author: windows-sdk-content
description: Instantiates a new instance of the Matrix3x2F class that contains the specified values.
old-location: direct2d\matrix3x2f_matrix3x2f_float__float__float__float__float__float_.htm
old-project: direct2d
ms.assetid: f4701597-9473-4333-9e6d-60000ccea40e
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: D2D1.Matrix3x2F.Matrix3x2F, D2D1::Matrix3x2F::Matrix3x2F, Matrix3x2F, Matrix3x2F constructor [Direct2D], Matrix3x2F constructor [Direct2D],Matrix3x2F interface, Matrix3x2F interface [Direct2D],Matrix3x2F constructor, Matrix3x2F.Matrix3x2F, Matrix3x2F.Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT), Matrix3x2F::Matrix3x2F, Matrix3x2F::Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT), d2d1helper/Matrix3x2F::Matrix3x2F, direct2d.matrix3x2f_matrix3x2f_float__float__float__float__float__float_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - Matrix3x2F.Matrix3x2F
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# Matrix3x2F::Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)


## -description


Instantiates a new instance of the <a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a> class that contains the specified values.


## -parameters




### -param m11




### -param m12




### -param m21




### -param m22




### -param m31




### -param m32






#### - _11

Type: <b>FLOAT</b>

The value in the first row and first column of the matrix.




#### - _12

Type: <b>FLOAT</b>

The value in the first row and second column of the matrix.




#### - _21

Type: <b>FLOAT</b>

The value in the second row and first column of the matrix.


#### - _22

Type: <b>FLOAT</b>

The value in the second row and second column of the matrix.


#### - _31

Type: <b>FLOAT</b>

The value in the third row and first column of the matrix.




#### - _32

Type: <b>FLOAT</b>

The value in the third row and second column of the matrix.




## -remarks



This method enables you to explicitly set the values of  matrix members. When using this method, ensure that each member represents an appropriate value for your transformation matrix. For example, to create the identity matrix, you must set <i>_11</i> and <i>_22</i> to 1, and the rest to 0. To create a translation matrix, you must set <i>_11</i> and <i>_22</i> to 1, <i>_12</i> and <i>_21</i> to 0, <i>_31</i> to the x displacement, and <i>_32</i> to the y displacement.

For convenience and accuracy, we recommended that whenever possible you use other helper functions, such as <a href="https://msdn.microsoft.com/c4596d43-fbc8-489e-a8fd-d33fb26461cc">Identity</a> and <a href="https://msdn.microsoft.com/eb289287-4f33-42cf-a306-120adda70371">Translation</a>, instead of this one.




## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

