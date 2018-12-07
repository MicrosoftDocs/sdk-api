---
UID: NF:winuser.InvalidateRect
title: InvalidateRect function
author: windows-sdk-content
description: The InvalidateRect function adds a rectangle to the specified window's update region. The update region represents the portion of the window's client area that must be redrawn.
old-location: gdi\invalidaterect.htm
tech.root: gdi
ms.assetid: 5a823d36-d08b-41c9-8857-540576f54b55
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InvalidateRect, InvalidateRect function [Windows GDI], _win32_InvalidateRect, gdi.invalidaterect, winuser/InvalidateRect
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
 - InvalidateRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InvalidateRect function


## -description


The <b>InvalidateRect</b> function adds a rectangle to the specified window's update region. The update region represents the portion of the window's client area that must be redrawn.


## -parameters




### -param hWnd [in]

A handle to the window whose update region has changed. If this parameter is <b>NULL</b>, the system invalidates and redraws all windows, not just the windows for this application, and sends the <a href="https://msdn.microsoft.com/en-us/library/ms648055(v=VS.85).aspx">WM_ERASEBKGND</a> and <a href="https://msdn.microsoft.com/d8a2a8b9-2c5d-484c-be09-67eb33de67c0">WM_NCPAINT</a> messages before the function returns. Setting this parameter to <b>NULL</b> is not recommended.


### -param lpRect [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the client coordinates of the rectangle to be added to the update region. If this parameter is <b>NULL</b>, the entire client area is added to the update region.


### -param bErase [in]

Specifies whether the background within the update region is to be erased when the update region is processed. If this parameter is <b>TRUE</b>, the background is erased when the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function is called. If this parameter is <b>FALSE</b>, the background remains unchanged.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The invalidated areas accumulate in the update region until the region is processed when the next <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message occurs or until the region is validated by using the <a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a> or <a href="https://msdn.microsoft.com/80fb1d4a-d9b1-4e67-b585-eee81893ed34">ValidateRgn</a> function.

The system sends a <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message to a window whenever its update region is not empty and there are no other messages in the application queue for that window.

If the <i>bErase</i> parameter is <b>TRUE</b> for any part of the update region, the background is erased in the entire region, not just in the specified part.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/41c2bc07-768b-4d27-a869-69b072f3e033">Invalidating the Client Area</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/b5b44efe-8045-4e54-89f9-1766689a053d">InvalidateRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a>



<a href="https://msdn.microsoft.com/80fb1d4a-d9b1-4e67-b585-eee81893ed34">ValidateRgn</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648055(v=VS.85).aspx">WM_ERASEBKGND</a>



<a href="https://msdn.microsoft.com/d8a2a8b9-2c5d-484c-be09-67eb33de67c0">WM_NCPAINT</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>
 

 

