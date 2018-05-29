---
UID: NF:d2d1helper.Matrix3x2F.Translation
title: Matrix3x2F::Translation
author: windows-sdk-content
description: Creates a translation transformation that has the specified x and y displacements.
old-location: direct2d\matrix3x2f_translation.htm
old-project: Direct2D
ms.assetid: eb289287-4f33-42cf-a306-120adda70371
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1.Matrix3x2F.Translation, D2D1::Matrix3x2F::Translation, Matrix3x2F class [Direct2D],Translation method, Matrix3x2F.Translation, Matrix3x2F::Translation, Matrix3x2F::Translation(D2D1_SIZE_F), Translation, Translation method [Direct2D], Translation method [Direct2D],Matrix3x2F class, d2d1helper/Matrix3x2F::Translation, direct2d.matrix3x2f_translation
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
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D2d1.dll
api_name:
-	Matrix3x2F.Translation
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# Matrix3x2F::Translation


## -description


Creates a translation transformation that has the specified x and y displacements.


## -parameters




#### - size

Type: <b><a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

The distance to translate along the x-axis and the y-axis.


## -returns



Type: <b><a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a></b>

A transformation matrix that translates an object the specified horizontal and vertical distance.




## -remarks



 Translation  is an affine transformation, which moves every point by a fixed distance in the same direction. It is similar to shifting the origin of the coordinate space. You can translate an object along the x-axis, the y-axis, or both. 

When calling this method, specify the x and y displacements and create  a <a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a> structure for storing the displacements.   If you prefer to specify each displacement as a parameter, call the  other <a href="https://msdn.microsoft.com/ec1a15f1-e2d5-482e-b688-10461e736934">Translation</a> method. The following illustration shows a square moved 20 pixels to the right along the x-axis, and 10 pixels downward along the y-axis.

<img alt="Illustration of a square moved to the right and down from its original position" src="images/translation_ovw.png"/>
 For an example, see <a href="https://msdn.microsoft.com/0fc48801-de14-4398-816d-6e7ddf4ffdd7">How to Translate an Object</a>.




## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

