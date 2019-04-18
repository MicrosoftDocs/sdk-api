---
UID: NF:gdipluspath.PathGradientBrush.SetGammaCorrection
title: PathGradientBrush::SetGammaCorrection (gdipluspath.h)
author: windows-sdk-content
description: The PathGradientBrush::SetGammaCorrection method specifies whether gamma correction is enabled for this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetGammaCorrection_useGammaCorrection_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setgammacorrection_7usegammacorrection.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetGammaCorrection method, PathGradientBrush.SetGammaCorrection, PathGradientBrush::SetGammaCorrection, SetGammaCorrection, SetGammaCorrection method [GDI+], SetGammaCorrection method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetGammaCorrection_useGammaCorrection_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetGammaCorrection_useGammaCorrection_
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
ms.custom: 19H1
---

# PathGradientBrush::SetGammaCorrection


## -description


The <b>PathGradientBrush::SetGammaCorrection</b> method specifies whether gamma correction is enabled for this path gradient brush.


## -parameters




### -param useGammaCorrection [in]

Type: <b>BOOL</b>

Boolean value that specifies whether gamma correction is enabled. <b>TRUE</b> specifies that gamma correction is enabled, and <b>FALSE</b> specifies that gamma correction is not enabled. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535066(v=VS.85).aspx">PathGradientBrush::GetGammaCorrection</a>
 

 

