---
UID: NF:winuser.ValidateRect
title: ValidateRect function
author: windows-sdk-content
description: The ValidateRect function validates the client area within a rectangle by removing the rectangle from the update region of the specified window.
old-location: gdi\validaterect.htm
tech.root: gdi
ms.assetid: 961dd768-1849-44df-bc7f-480881ed6477
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ValidateRect, ValidateRect function [Windows GDI], _win32_ValidateRect, gdi.validaterect, winuser/ValidateRect
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
 - ValidateRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ValidateRect function


## -description


The <b>ValidateRect</b> function validates the client area within a rectangle by removing the rectangle from the update region of the specified window.


## -parameters




### -param hWnd [in]

Handle to the window whose update region is to be modified. If this parameter is <b>NULL</b>, the system invalidates and redraws all windows and sends the <b>WM_ERASEBKGND</b> and <b>WM_NCPAINT</b> messages to the window procedure before the function returns.


### -param lpRect [in]

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the client coordinates of the rectangle to be removed from the update region. If this parameter is <b>NULL</b>, the entire client area is removed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function automatically validates the entire client area. Neither the <b>ValidateRect</b> nor <a href="https://msdn.microsoft.com/80fb1d4a-d9b1-4e67-b585-eee81893ed34">ValidateRgn</a> function should be called if a portion of the update region must be validated before the next <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message is generated.

The system continues to generate <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> messages until the current update region is validated.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a>



<a href="https://msdn.microsoft.com/b5b44efe-8045-4e54-89f9-1766689a053d">InvalidateRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/80fb1d4a-d9b1-4e67-b585-eee81893ed34">ValidateRgn</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>
 

 

