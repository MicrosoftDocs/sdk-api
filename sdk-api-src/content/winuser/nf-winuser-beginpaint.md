---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

