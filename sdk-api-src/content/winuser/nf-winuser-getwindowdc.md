---
UID: NF:winuser.GetWindowDC
title: GetWindowDC function
author: windows-sdk-content
description: The GetWindowDC function retrieves the device context (DC) for the entire window, including title bar, menus, and scroll bars.
old-location: gdi\getwindowdc.htm
tech.root: gdi
ms.assetid: 9e6a135e-e337-4129-a3ad-faf9a8ac9b2d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetWindowDC, GetWindowDC function [Windows GDI], _win32_GetWindowDC, gdi.getwindowdc, winuser/GetWindowDC
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
 - GetWindowDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWindowDC function


## -description


The <b>GetWindowDC</b> function retrieves the device context (DC) for the entire window, including title bar, menus, and scroll bars. A window device context permits painting anywhere in a window, because the origin of the device context is the upper-left corner of the window instead of the client area.

<b>GetWindowDC</b> assigns default attributes to the window device context each time it retrieves the device context. Previous attributes are lost.


## -parameters




### -param hWnd [in]

A handle to the window with a device context that is to be retrieved. If this value is <b>NULL</b>, <b>GetWindowDC</b> retrieves the device context for the entire screen.

If this parameter is <b>NULL</b>, <b>GetWindowDC</b> retrieves the device context for the primary display monitor. To get the device context for other display monitors, use the <a href="https://msdn.microsoft.com/a7668c28-77c9-4373-ae1a-eab3cb98f866">EnumDisplayMonitors</a> and <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a> functions.


## -returns



If the function succeeds, the return value is a handle to a device context for the specified window.

If the function fails, the return value is <b>NULL</b>, indicating an error or an invalid <i>hWnd</i> parameter.




## -remarks



<b>GetWindowDC</b> is intended for special painting effects within a window's nonclient area. Painting in nonclient areas of any window is not recommended.

The <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function can be used to retrieve the dimensions of various parts of the nonclient area, such as the title bar, menu, and scroll bars.

The <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a> function can be used to retrieve a device context for the entire screen.

After painting is complete, the <a href="https://msdn.microsoft.com/c4f48f1e-4a37-4330-908e-2ac5c65e1a1d">ReleaseDC</a> function must be called to release the device context. Not releasing the window device context has serious effects on painting requested by applications.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>



<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/c4f48f1e-4a37-4330-908e-2ac5c65e1a1d">ReleaseDC</a>
 

 

