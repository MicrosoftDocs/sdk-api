---
UID: NF:winddi.EngCreateWnd
title: EngCreateWnd function
author: windows-sdk-content
description: The EngCreateWnd function creates a WNDOBJ structure for the window referenced by hwnd.
old-location: display\engcreatewnd.htm
tech.root: display
ms.assetid: 14b1cced-32d0-4ba8-be7c-e626bef37e3f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngCreateWnd, EngCreateWnd function [Display Devices], display.engcreatewnd, gdifncs_71294a09-97a4-41c5-9ddb-2295febc73a2.xml, winddi/EngCreateWnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngCreateWnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngCreateWnd function


## -description


The <b>EngCreateWnd</b> function creates a <a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a> structure for the window referenced by <i>hwnd</i>.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure identifying a device surface.


### -param hwnd

Handle to the window created by an application's call to the Win32 <b>CreateWindow</b> or equivalent function.


### -param pfn





###### 


### -param fl

Is a bitmask that specifies the type of changes GDI should track and report to the driver. This value must be consistent through all <a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a> requests made by the driver. This parameter can be one or more of the following bitfield values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
WO_DRAW_NOTIFY

</td>
<td>
GDI should provide the driver with WOC_DRAWN notifications.

</td>
</tr>
<tr>
<td>
WO_RGN_CLIENT

</td>
<td>
GDI should track changes in the client region of the window object, and notify the driver when the window's visible client region changes. The region enumerated in the callback function is the new visible client area of the window.

</td>
</tr>
<tr>
<td>
WO_RGN_CLIENT_DELTA

</td>
<td>
GDI should track changes in the delta client region of the window object, and notify the driver when the window's visible region changes. The region enumerated in the callback function is a nonempty delta area that is in the new region but not in the old region. The delta region is valid during the callback only.

</td>
</tr>
<tr>
<td>
WO_RGN_DESKTOP_COORD

</td>
<td>
GDI creates a WNDOBJ structure with desktop coordinates when the system is running multiple monitors.

GDI ignores this flag and creates a WNDOBJ structure with device coordinates when the system is running a single monitor.

</td>
</tr>
<tr>
<td>
WO_RGN_SURFACE

</td>
<td>
GDI should track changes in the surface region of the window object, and notify the driver when the surface region changes. The surface region is the display surface area excluding all visible client regions of the windows being tracked by the driver.

</td>
</tr>
<tr>
<td>
WO_RGN_SURFACE_DELTA

</td>
<td>
GDI should track changes in the delta surface region of the window object, and notify the driver when the surface region changes. The region enumerated in the callback function is a nonempty delta area that is in the new surface region but not in the old surface region. The delta surface region is valid during the callback only.

</td>
</tr>
<tr>
<td>
WO_RGN_UPDATE_ALL

</td>
<td>
GDI should notify the driver for all windows it tracks when any of its windows' visible regions change. This flag must be used in conjunction with the WO_RGN_CLIENT flag.

</td>
</tr>
<tr>
<td>
WO_RGN_WINDOW

</td>
<td>
GDI should track changes in the entire region of the window object (which includes the client region of the window), and notify the driver when the window's region changes.

</td>
</tr>
<tr>
<td>
WO_SPRITE_NOTIFY

</td>
<td>
GDI should notify the driver for all windows it tracks when any of its windows' visible regions are overlapped or no longer overlapped by sprites.

</td>
</tr>
</table>
 


### -param iPixelFormat

Specifies the pixel format associated with the window object. The pixel format of a window object is fixed. This parameter can be zero if there is no associated pixel format.


## -returns



The return value is a pointer to a <a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a> structure if the function is successful. Otherwise, the return value is −1 if the same window is being tracked by the driver, or zero if the driver is not tracking the same window.




## -remarks



Because creating a window object involves locking window resources, <b>EngCreateWnd</b> should be called only in the context of the WNDOBJ_SETUP escape in <a href="https://msdn.microsoft.com/7b59dc85-27f4-4529-847e-6027dae8a45a">DrvEscape</a>.

<b>EngCreateWnd</b> supports window tracking by multiple drivers, where each driver is identified by a unique <a href="https://msdn.microsoft.com/09213eb9-df62-4da9-a221-3b50e66f5c68">WNDOBJCHANGEPROC</a> function pointer identified by <i>pfn</i>. For example, a live video driver can track changes to live video windows while an OpenGL driver is tracking changes to OpenGL windows.

GDI will call <b>WNDOBJCHANGEPROC</b> with the most recent window state if a new <a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a> is created by <i>DrvEscape</i>. GDI will also notify <b>WNDOBJCHANGEPROC</b> when a window described by a WNDOBJ structure is destroyed.

The WOC_SPRITE_OVERLAP and WOC_SPRITE_NO_OVERLAP notifications passed to <b>WNDOBJCHANGEPROC</b> allow the driver to be synchronously informed when a sprite is on top of its window, and take the appropriate action. The driver receives these notifications even if all sprites have been torn down by the ECS_TEARDOWN flag of <a href="https://msdn.microsoft.com/8de02019-6f58-4adc-9589-fdfbf4a062aa">EngControlSprites</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b59dc85-27f4-4529-847e-6027dae8a45a">DrvEscape</a>



<a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a>



<a href="https://msdn.microsoft.com/09213eb9-df62-4da9-a221-3b50e66f5c68">WNDOBJCHANGEPROC</a>
 

 

