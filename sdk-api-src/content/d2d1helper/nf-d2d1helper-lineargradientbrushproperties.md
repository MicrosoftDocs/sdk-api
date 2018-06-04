---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# LinearGradientBrushProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/753278f0-d8a1-4dc5-b976-a00f8aab357e">D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</a> structure.


## -parameters




### -param startPoint [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The start point, in the brush's coordinate space, of the gradient axis. 


### -param endPoint [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The end point, in the brush's coordinate space, of the gradient axis.


## -returns



Type: <b><a href="https://msdn.microsoft.com/753278f0-d8a1-4dc5-b976-a00f8aab357e">D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</a></b>

A structure that contains the start and end point of the gradient axis for an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>.



