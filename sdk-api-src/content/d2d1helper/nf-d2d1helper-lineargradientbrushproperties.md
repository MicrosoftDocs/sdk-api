---
UID: NF:d2d1helper.LinearGradientBrushProperties
title: LinearGradientBrushProperties function
author: windows-sdk-content
description: Creates a D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES structure.
old-location: direct2d\lineargradientbrushproperties.htm
tech.root: direct2d
ms.assetid: dba59936-2b2d-4a9b-aba4-acb6ff84c037
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: LinearGradientBrushProperties, LinearGradientBrushProperties function [Direct2D], d2d1helper/LinearGradientBrushProperties, direct2d.lineargradientbrushproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - LinearGradientBrushProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



