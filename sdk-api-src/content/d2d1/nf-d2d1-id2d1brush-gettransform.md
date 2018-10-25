---
UID: NF:d2d1.ID2D1Brush.GetTransform
title: ID2D1Brush::GetTransform
author: windows-sdk-content
description: Gets the transform applied to this brush.
old-location: direct2d\ID2D1Brush_GetTransform.htm
tech.root: direct2d
ms.assetid: f28282e8-f994-4501-a327-fcceb8379f70
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetTransform, GetTransform method [Direct2D], GetTransform method [Direct2D],ID2D1Brush interface, ID2D1Brush interface [Direct2D],GetTransform method, ID2D1Brush.GetTransform, ID2D1Brush::GetTransform, d2d1/ID2D1Brush::GetTransform, direct2d.ID2D1Brush_GetTransform
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
 - ID2D1Brush.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Brush::GetTransform


## -description


Gets the transform applied to this brush.


## -parameters




### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform applied to this brush.


## -returns



This method does not return a value.




## -remarks



When the brush transform is the identity matrix, the brush appears in the same coordinate space as the render target in which it is drawn.




## -see-also




<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>
 

 

