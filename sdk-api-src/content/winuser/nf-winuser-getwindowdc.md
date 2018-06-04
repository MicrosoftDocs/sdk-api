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
 

 

