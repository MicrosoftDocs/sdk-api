---
UID: NF:d2d1helper.Matrix3x2F.Scale(D2D1_SIZE_F,D2D1_POINT_2F)
title: Matrix3x2F::Scale(D2D1_SIZE_F,D2D1_POINT_2F)
author: windows-sdk-content
description: Creates a scale transformation that has the specified scale factors and center point.
old-location: direct2d\matrix3x2f_scale_d2d1_size_f_d2d1_point_2f_.htm
tech.root: direct2d
ms.assetid: c2aa64eb-c69a-4938-91de-1541f1c7844f
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D2D1.Matrix3x2F.Scale, D2D1::Matrix3x2F::Scale, Matrix3x2F class [Direct2D],Scale method, Matrix3x2F.Scale, Matrix3x2F.Scale(D2D1_SIZE_F,D2D1_POINT_2F), Matrix3x2F::Scale, Matrix3x2F::Scale(D2D1_SIZE_F,D2D1_POINT_2F), Scale, Scale method [Direct2D], Scale method [Direct2D],Matrix3x2F class, d2d1helper/Matrix3x2F::Scale, direct2d.matrix3x2f_scale_d2d1_size_f_d2d1_point_2f_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Matrix3x2F.Scale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Matrix3x2F::Scale(D2D1_SIZE_F,D2D1_POINT_2F)


## -description


Creates a scale transformation that has the specified scale factors and center point. 


## -parameters




### -param size

Type: <b><a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

The x-axis and y-axis scale factors of the scale transformation.


### -param center

TBD




#### - centerPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point about which the scale is performed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a></b>

The new scale transformation.




## -remarks



This method creates a scale transformation for the specified <i>centerPoint</i> and scale factors. The scale factors are stored as an ordered pair in the 
	 <a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a> structure. If you prefer to list each scale factor as a parameter, call the other <a href="https://msdn.microsoft.com/401b8710-c486-44b0-b79c-d7238279fdef">Scale</a> method. 

The following illustration shows the size of the square increased 
	 to 130% in each dimension.
	 The center point for the scaling is the upper-left corner of the square.

<img alt="Illustration of a square scaled by 130% in the x-direction and y-direction" src="images/scale_ovw.png"/>

 For an example, see <a href="https://msdn.microsoft.com/3da749e2-50d5-4f4e-9ccd-8c230efe3436">How to Scale an Object</a>.




## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

