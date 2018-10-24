---
UID: NF:gdipluspath.PathGradientBrush.SetGammaCorrection
title: PathGradientBrush::SetGammaCorrection
author: windows-sdk-content
description: The PathGradientBrush::SetGammaCorrection method specifies whether gamma correction is enabled for this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetGammaCorrection_useGammaCorrection_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setgammacorrection_7usegammacorrection.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PathGradientBrush class [GDI+],SetGammaCorrection method, PathGradientBrush.SetGammaCorrection, PathGradientBrush::SetGammaCorrection, SetGammaCorrection, SetGammaCorrection method [GDI+], SetGammaCorrection method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetGammaCorrection_useGammaCorrection_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetGammaCorrection_useGammaCorrection_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
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
 - PathGradientBrush.SetGammaCorrection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetGammaCorrection


## -description


The <b>PathGradientBrush::SetGammaCorrection</b> method specifies whether gamma correction is enabled for this path gradient brush.


## -parameters




### -param useGammaCorrection [in]

Type: <b>BOOL</b>

Boolean value that specifies whether gamma correction is enabled. <b>TRUE</b> specifies that gamma correction is enabled, and <b>FALSE</b> specifies that gamma correction is not enabled. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/8b2b6c00-2625-42f7-a114-10a0872b7884">PathGradientBrush::GetGammaCorrection</a>
 

 

