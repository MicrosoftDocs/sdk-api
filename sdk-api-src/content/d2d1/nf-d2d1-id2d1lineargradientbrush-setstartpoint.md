---
UID: NF:d2d1.ID2D1LinearGradientBrush.SetStartPoint
title: ID2D1LinearGradientBrush::SetStartPoint
author: windows-sdk-content
description: Sets the starting coordinates of the linear gradient in the brush's coordinate space.
old-location: direct2d\ID2D1LinearGradientBrush_SetStartPoint.htm
tech.root: Direct2D
ms.assetid: f70ab519-f64f-4c33-8239-83e093560418
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1LinearGradientBrush interface [Direct2D],SetStartPoint method, ID2D1LinearGradientBrush.SetStartPoint, ID2D1LinearGradientBrush::SetStartPoint, SetStartPoint, SetStartPoint method [Direct2D], SetStartPoint method [Direct2D],ID2D1LinearGradientBrush interface, d2d1/ID2D1LinearGradientBrush::SetStartPoint, direct2d.ID2D1LinearGradientBrush_SetStartPoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
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
req.namespace: 
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
 - ID2D1LinearGradientBrush.SetStartPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1LinearGradientBrush.SetStartPoint
: 
---

# ID2D1LinearGradientBrush::SetStartPoint


## -description


Sets the starting coordinates of the linear gradient in the brush's coordinate space. 


## -parameters




### -param startPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The starting two-dimensional coordinates of the linear gradient, in the brush's coordinate space.


## -returns



This method does not return a value.




## -remarks



The start point and end point are described in the brush's space and are mapped to the render target when the brush is used.  If there is a non-identity brush transform or render target transform, the brush's start point and end point are also transformed.




## -see-also




<a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>
 

 

