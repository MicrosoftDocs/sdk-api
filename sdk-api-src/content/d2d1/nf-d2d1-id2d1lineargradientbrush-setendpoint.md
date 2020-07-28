---
UID: NF:d2d1.ID2D1LinearGradientBrush.SetEndPoint
title: ID2D1LinearGradientBrush::SetEndPoint (d2d1.h)
description: Sets the ending coordinates of the linear gradient in the brush's coordinate space.
helpviewer_keywords: ["ID2D1LinearGradientBrush interface [Direct2D]","SetEndPoint method","ID2D1LinearGradientBrush.SetEndPoint","ID2D1LinearGradientBrush::SetEndPoint","SetEndPoint","SetEndPoint method [Direct2D]","SetEndPoint method [Direct2D]","ID2D1LinearGradientBrush interface","d2d1/ID2D1LinearGradientBrush::SetEndPoint","direct2d.ID2D1LinearGradientBrush_SetEndPoint"]
old-location: direct2d\ID2D1LinearGradientBrush_SetEndPoint.htm
tech.root: Direct2D
ms.assetid: b4d64f42-6038-442e-8666-0555a3e4ed75
ms.date: 12/05/2018
ms.keywords: ID2D1LinearGradientBrush interface [Direct2D],SetEndPoint method, ID2D1LinearGradientBrush.SetEndPoint, ID2D1LinearGradientBrush::SetEndPoint, SetEndPoint, SetEndPoint method [Direct2D], SetEndPoint method [Direct2D],ID2D1LinearGradientBrush interface, d2d1/ID2D1LinearGradientBrush::SetEndPoint, direct2d.ID2D1LinearGradientBrush_SetEndPoint
f1_keywords:
- d2d1/ID2D1LinearGradientBrush.SetEndPoint
dev_langs:
- c++
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
- ID2D1LinearGradientBrush.SetEndPoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1LinearGradientBrush::SetEndPoint


## -description


Sets the ending coordinates of the linear gradient in the brush's coordinate space.


## -parameters




### -param endPoint

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The ending two-dimensional coordinates of the linear gradient, in the brush's coordinate space.


## -remarks



The start point and end point are described in the brush's space and are mapped to the render target when the brush is used.  If there is a non-identity brush transform or render target transform, the brush's start point and end point are also transformed.




## -see-also




<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>
 

 

