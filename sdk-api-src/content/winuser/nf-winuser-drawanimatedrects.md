---
UID: NF:winuser.DrawAnimatedRects
title: DrawAnimatedRects function (winuser.h)
author: windows-sdk-content
description: Animates the caption of a window to indicate the opening of an icon or the minimizing or maximizing of a window.
old-location: gdi\drawanimatedrects.htm
tech.root: gdi
ms.assetid: 54a9234a-0056-4cfe-9158-86635dc31bc6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawAnimatedRects, DrawAnimatedRects function [Windows GDI], _win32_DrawAnimatedRects, gdi.drawanimatedrects, winuser/DrawAnimatedRects
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
 - DrawAnimatedRects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrawAnimatedRects function


## -description


Animates the caption of a window to indicate the opening of an icon or the minimizing or maximizing of a window.


## -parameters




### -param hwnd [in]

A handle to the window whose caption should be animated on the screen. The animation will be clipped to the parent of this window.


### -param idAni [in]

The type of animation. This must be IDANI_CAPTION. With the IDANI_CAPTION animation type, the window caption will animate from the position specified by lprcFrom to the position specified by lprcTo. The effect is similar to minimizing or maximizing a window.


### -param lprcFrom

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure specifying the location and size of the icon or minimized window. Coordinates are relative to the clipping window <i>hwnd</i>.


### -param lprcTo

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure specifying the location and size of the restored window. Coordinates are relative to the clipping window <i>hwnd</i>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>
 

 

