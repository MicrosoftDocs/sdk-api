---
UID: NF:winuser.PaintDesktop
title: PaintDesktop function
author: windows-sdk-content
description: The PaintDesktop function fills the clipping region in the specified device context with the desktop pattern or wallpaper. The function is provided primarily for shell desktops.
old-location: gdi\paintdesktop.htm
tech.root: gdi
ms.assetid: 738500d4-32f5-43cf-8d40-9ad201ca6d4b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PaintDesktop, PaintDesktop function [Windows GDI], _win32_PaintDesktop, gdi.paintdesktop, winuser/PaintDesktop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - PaintDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PaintDesktop
: 
---

# PaintDesktop function


## -description


The <b>PaintDesktop</b> function fills the clipping region in the specified device context with the desktop pattern or wallpaper. The function is provided primarily for shell desktops.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

