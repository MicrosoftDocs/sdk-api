---
UID: NF:winuser.DrawFocusRect
title: DrawFocusRect function
author: windows-sdk-content
description: The DrawFocusRect function draws a rectangle in the style used to indicate that the rectangle has the focus.
old-location: gdi\drawfocusrect.htm
tech.root: gdi
ms.assetid: a910d04f-fe4d-4fc9-a518-abac864da6f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawFocusRect, DrawFocusRect function [Windows GDI], _win32_DrawFocusRect, gdi.drawfocusrect, winuser/DrawFocusRect
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
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - DrawFocusRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawFocusRect function


## -description


The <b>DrawFocusRect</b> function draws a rectangle in the style used to indicate that the rectangle has the focus.


## -parameters




### -param hDC [in]

A handle to the device context.


### -param lprc [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the logical coordinates of the rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



<b>DrawFocusRect</b> works only in MM_TEXT mode.

Because <b>DrawFocusRect</b> is an XOR function, calling it a second time with the same rectangle removes the rectangle from the screen.

This function draws a rectangle that cannot be scrolled. To scroll an area containing a rectangle drawn by this function, call <b>DrawFocusRect</b> to remove the rectangle from the screen, scroll the area, and then call <b>DrawFocusRect</b> again to draw the rectangle in the new position.

<b>Windows XP:</b> The focus rectangle can now be thicker than 1 pixel, so it is more visible for high-resolution, high-density displays and accessibility needs. This is handled by the SPI_SETFOCUSBORDERWIDTH and SPI_SETFOCUSBORDERHEIGHT in <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>.


#### Examples

For an example, see "Creating an Owner-Drawn List Box" in <a href="_win32_Using_List_Boxes_cpp">Using List Boxes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a1083cb5-5e6c-4134-badf-9fc5142d1453">FrameRect</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>
 

 

