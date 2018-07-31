---
UID: NF:winuser.GetUpdateRect
title: GetUpdateRect function
author: windows-sdk-content
description: The GetUpdateRect function retrieves the coordinates of the smallest rectangle that completely encloses the update region of the specified window.
old-location: gdi\getupdaterect.htm
old-project: gdi
ms.assetid: e54483a1-8738-4b22-a24e-c0b31f6ca9d6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetUpdateRect, GetUpdateRect function [Windows GDI], _win32_GetUpdateRect, gdi.getupdaterect, winuser/GetUpdateRect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
 - GetUpdateRect
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetUpdateRect function


## -description


The <b>GetUpdateRect</b> function retrieves the coordinates of the smallest rectangle that completely encloses the update region of the specified window. <b>GetUpdateRect</b> retrieves the rectangle in logical coordinates. If there is no update region, <b>GetUpdateRect</b> retrieves an empty rectangle (sets all coordinates to zero).


## -parameters




### -param hWnd [in]

Handle to the window whose update region is to be retrieved.


### -param lpRect [out]

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the coordinates, in device units, of the enclosing rectangle.

An application can set this parameter to <b>NULL</b> to determine whether an update region exists for the window. If this parameter is <b>NULL</b>, <b>GetUpdateRect</b> returns nonzero if an update region exists, and zero if one does not. This provides a simple and efficient means of determining whether a <b>WM_PAINT</b> message resulted from an invalid area.


### -param bErase [in]

Specifies whether the background in the update region is to be erased. If this parameter is <b>TRUE</b> and the update region is not empty, <b>GetUpdateRect</b> sends a <b>WM_ERASEBKGND</b> message to the specified window to erase the background.


## -returns



If the update region is not empty, the return value is nonzero.

If there is no update region, the return value is zero.




## -remarks



The update rectangle retrieved by the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function is identical to that retrieved by <b>GetUpdateRect</b>.


<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> automatically validates the update region, so any call to <b>GetUpdateRect</b> made immediately after the call to <b>BeginPaint</b> retrieves an empty update region.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/d80c4b44-3f50-46f9-bf5a-fff7868d91ba">GetUpdateRgn</a>



<a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a>



<a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a>
 

 

