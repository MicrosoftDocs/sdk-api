---
UID: NF:gdiplusbrush.LinearGradientBrush.SetLinearColors
title: LinearGradientBrush::SetLinearColors
author: windows-sdk-content
description: The LinearGradientBrush::SetLinearColors method sets the starting color and ending color of this linear gradient brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setlinearcolors.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LinearGradientBrush class [GDI+],SetLinearColors method, LinearGradientBrush.SetLinearColors, LinearGradientBrush::SetLinearColors, SetLinearColors, SetLinearColors method [GDI+], SetLinearColors method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.SetLinearColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::SetLinearColors


## -description


The <b>LinearGradientBrush::SetLinearColors</b> method sets the starting color and ending color of this linear gradient brush.


## -parameters




### -param color1 [in]

Type: <b>const Color&amp;</b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush. 


### -param color2 [in]

Type: <b>const Color&amp;</b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/9b0236b2-be6b-4918-a106-5b0e6c3dd5ff">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/0849880c-3a52-4614-bc32-cc120ff5a90f">LinearGradientBrush::GetLinearColors</a>



<a href="https://msdn.microsoft.com/3fbdebd7-e988-4e2e-8bfe-dbac9a34fff7">LinearGradientBrush::SetInterpolationColors</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>
 

 

