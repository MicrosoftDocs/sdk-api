---
UID: NF:winuser.BeginPaint
title: BeginPaint function
author: windows-driver-content
description: The BeginPaint function prepares the specified window for painting and fills a PAINTSTRUCT structure with information about the painting.
old-location: gdi\beginpaint.htm
old-project: gdi
ms.assetid: 513341d7-bed8-469c-a067-ee71dc8860f9
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: BeginPaint, BeginPaint function [Windows GDI], _win32_BeginPaint, gdi.beginpaint, winuser/BeginPaint
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	user32.dll
-	Ext-MS-Win-NTUser-Draw-l1-1-0.dll
-	Ext-MS-Win-NTUser-Draw-l1-1-1.dll
-	ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
-	BeginPaint
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# BeginPaint function


## -description


The <b>BeginPaint</b> function prepares the specified window for painting and fills a <a href="https://msdn.microsoft.com/1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433">PAINTSTRUCT</a> structure with information about the painting.


## -parameters




### -param hWnd

TBD


### -param lpPaint [out]

Pointer to the <a href="https://msdn.microsoft.com/1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433">PAINTSTRUCT</a> structure that will receive painting information.


#### - hwnd [in]

Handle to the window to be repainted.


## -returns



If the function succeeds, the return value is the handle to a display device context for the specified window.

If the function fails, the return value is <b>NULL</b>, indicating that no display device context is available.




## -remarks



The <b>BeginPaint</b> function automatically sets the clipping region of the device context to exclude any area outside the update region. The update region is set by the <a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a> or <a href="https://msdn.microsoft.com/b5b44efe-8045-4e54-89f9-1766689a053d">InvalidateRgn</a> function and by the system after sizing, moving, creating, scrolling, or any other operation that affects the client area. If the update region is marked for erasing, <b>BeginPaint</b> sends a <b>WM_ERASEBKGND</b> message to the window.

An application should not call <b>BeginPaint</b> except in response to a <b>WM_PAINT</b> message. Each call to <b>BeginPaint</b> must have a corresponding call to the <a href="https://msdn.microsoft.com/b07cfed9-21c4-4459-855a-eaf4d1d34ab8">EndPaint</a> function.

If the caret is in the area to be painted, <b>BeginPaint</b> automatically hides the caret to prevent it from being erased.

If the window's class has a background brush, <b>BeginPaint</b> uses that brush to erase the background of the update region before returning.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is always in terms of physical pixels.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/ed995bfd-a791-4d73-9a0b-daf65a9f7709">Drawing in the Client Area</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b07cfed9-21c4-4459-855a-eaf4d1d34ab8">EndPaint</a>



<a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a>



<a href="https://msdn.microsoft.com/b5b44efe-8045-4e54-89f9-1766689a053d">InvalidateRgn</a>



<a href="https://msdn.microsoft.com/1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433">PAINTSTRUCT</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a>



<a href="https://msdn.microsoft.com/80fb1d4a-d9b1-4e67-b585-eee81893ed34">ValidateRgn</a>
 

 

