---
UID: NF:d2d1helper.GradientStop
title: GradientStop function
author: windows-sdk-content
description: Creates a D2D1_GRADIENT_STOP structure.
old-location: direct2d\gradientstop.htm
old-project: direct2d
ms.assetid: 37f413e8-36ee-462d-8419-908690094c49
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GradientStop, GradientStop function [Direct2D], d2d1helper/GradientStop, direct2d.gradientstop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1helper.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - GradientStop
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# GradientStop function


## -description


Creates a <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structure. 


## -parameters




### -param position

Type: <b>FLOAT</b>

A value that indicates the relative position of the gradient stop in the brush. A value of 0.0 specifies that the stop is positioned at the beginning of the gradient vector, while a value of 1.0 specifies that the stop is positioned at the end of the gradient vector. Stops outside the 0.0-1.0 range might not be directly visible but still influence the gradient pattern.


### -param color [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color of the gradient stop.




## -returns



Type: <b><a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a></b>

The new gradient stop.




## -see-also




<a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>



<a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>
 

 

