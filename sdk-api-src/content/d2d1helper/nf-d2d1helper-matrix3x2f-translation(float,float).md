---
UID: NF:d2d1helper.Matrix3x2F.Translation(FLOAT,FLOAT)
title: Matrix3x2F::Translation(FLOAT,FLOAT)
author: windows-sdk-content
description: Creates a translation transformation that has the specified x and y displacements.
old-location: direct2d\matrix3x2f_translation_float_float_.htm
tech.root: Direct2D
ms.assetid: ec1a15f1-e2d5-482e-b688-10461e736934
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: D2D1.Matrix3x2F.Translation, D2D1::Matrix3x2F::Translation, Matrix3x2F class [Direct2D],Translation method, Matrix3x2F.Translation, Matrix3x2F.Translation(FLOAT,FLOAT), Matrix3x2F::Translation, Matrix3x2F::Translation(FLOAT,FLOAT), Translation, Translation method [Direct2D], Translation method [Direct2D],Matrix3x2F class, d2d1helper/Matrix3x2F::Translation, direct2d.matrix3x2f_translation_float_float_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - Matrix3x2F.Translation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Matrix3x2F::Translation(FLOAT,FLOAT)


## -description


Creates a translation transformation that has the specified x and y displacements.


## -parameters




### -param x

Type: <b>FLOAT</b>

The distance to translate along the x-axis.


### -param y

Type: <b>FLOAT</b>

The distance to translate along the y-axis.


## -returns



Type: <b><a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a></b>

A transformation matrix that translates an object the specified horizontal and vertical distance.




## -remarks



 Translation  is an affine transformation, which moves every point by a fixed distance in the same direction. It is similar to shifting the origin of the coordinate space. You can translate an object along the x-axis, the y-axis, or both. 

When calling this method, specify the x and y displacements. If you prefer to define both displacements in an ordered pair by using the <a href="https://msdn.microsoft.com/en-us/library/Dd368160(v=VS.85).aspx">D2D1_SIZE_F</a> structure, call the  other <a href="https://msdn.microsoft.com/eb289287-4f33-42cf-a306-120adda70371">Translation</a> method. The following illustration shows a square moved 20 pixels to the right along the x-axis, and 10 pixels downward along the y-axis.

<img alt="Illustration of the square moved to the right and downward" src="./images/translation_ovw.png"/>
 For an example, see <a href="https://msdn.microsoft.com/en-us/library/Dd756691(v=VS.85).aspx">How to Translate an Object</a>.




## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

