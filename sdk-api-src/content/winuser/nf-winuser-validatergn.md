---
UID: NF:winuser.ValidateRgn
title: ValidateRgn function
author: windows-sdk-content
description: The ValidateRgn function validates the client area within a region by removing the region from the current update region of the specified window.
old-location: gdi\validatergn.htm
tech.root: gdi
ms.assetid: 80fb1d4a-d9b1-4e67-b585-eee81893ed34
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ValidateRgn, ValidateRgn function [Windows GDI], _win32_ValidateRgn, gdi.validatergn, winuser/ValidateRgn
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
 - ValidateRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ValidateRgn
: 
---

# ValidateRgn function


## -description


The <b>ValidateRgn</b> function validates the client area within a region by removing the region from the current update region of the specified window.


## -parameters




### -param hWnd [in]

Handle to the window whose update region is to be modified.


### -param hRgn [in]

Handle to a region that defines the area to be removed from the update region. If this parameter is <b>NULL</b>, the entire client area is removed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The specified region must have been created by a region function. The region coordinates are assumed to be client coordinates.

The <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function automatically validates the entire client area. Neither the <a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a> nor <b>ValidateRgn</b> function should be called if a portion of the update region must be validated before the next <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message is generated.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/408fda82-30c3-4eb4-be42-3085c71ba99e">ExcludeUpdateRgn</a>



<a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a>



<a href="https://msdn.microsoft.com/b5b44efe-8045-4e54-89f9-1766689a053d">InvalidateRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>
 

 

