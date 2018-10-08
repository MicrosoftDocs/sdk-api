---
UID: NF:d2d1.ID2D1LinearGradientBrush.GetStartPoint
title: ID2D1LinearGradientBrush::GetStartPoint
author: windows-sdk-content
description: Retrieves the starting coordinates of the linear gradient.
old-location: direct2d\ID2D1LinearGradientBrush_GetStartPoint.htm
tech.root: Direct2D
ms.assetid: 8b79b265-4bf4-48e7-99c9-64a52d8cb6d0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetStartPoint, GetStartPoint method [Direct2D], GetStartPoint method [Direct2D],ID2D1LinearGradientBrush interface, ID2D1LinearGradientBrush interface [Direct2D],GetStartPoint method, ID2D1LinearGradientBrush.GetStartPoint, ID2D1LinearGradientBrush::GetStartPoint, d2d1/ID2D1LinearGradientBrush::GetStartPoint, direct2d.ID2D1LinearGradientBrush_GetStartPoint
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
 - ID2D1LinearGradientBrush.GetStartPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1LinearGradientBrush::GetStartPoint


## -description


Retrieves the starting coordinates of the linear gradient.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The starting two-dimensional coordinates of the linear gradient, in the brush's coordinate space.




## -remarks



The start point and end point are described in the brush's space and are mapped to the render target when the brush is used.  If there is a non-identity brush transform or render target transform, the brush's start point and end point are also transformed.




## -see-also




<a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>
 

 

