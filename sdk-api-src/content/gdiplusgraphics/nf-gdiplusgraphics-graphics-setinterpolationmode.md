---
UID: NF:gdiplusgraphics.Graphics.SetInterpolationMode
title: Graphics::SetInterpolationMode
author: windows-sdk-content
description: The Graphics::SetInterpolationMode method sets the interpolation mode of this Graphics object. The interpolation mode determines the algorithm that is used when images are scaled or rotated.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setinterpolationmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Graphics class [GDI+],SetInterpolationMode method, Graphics.SetInterpolationMode, Graphics::SetInterpolationMode, SetInterpolationMode, SetInterpolationMode method [GDI+], SetInterpolationMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_, gdiplus._gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.SetInterpolationMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::SetInterpolationMode


## -description


The <b>Graphics::SetInterpolationMode</b> method sets the interpolation mode of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. The interpolation mode determines the algorithm that is used when images are scaled or rotated.


## -parameters




### -param interpolationMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534141(v=VS.85).aspx">InterpolationMode</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534141(v=VS.85).aspx">InterpolationMode</a> enumeration that specifies the interpolation mode. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535711(v=VS.85).aspx">Graphics::GetInterpolationMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534141(v=VS.85).aspx">InterpolationMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533836(v=VS.85).aspx">Using Interpolation Mode to Control Image Quality During Scaling</a>
 

 

