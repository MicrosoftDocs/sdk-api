---
UID: NF:winuser.EnumDisplayMonitors
title: EnumDisplayMonitors function
author: windows-driver-content
description: The EnumDisplayMonitors function enumerates display monitors (including invisible pseudo-monitors associated with the mirroring drivers) that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context. EnumDisplayMonitors calls an application-defined MonitorEnumProc callback function once for each monitor that is enumerated. Note that GetSystemMetrics (SM_CMONITORS) counts only the display monitors.
old-location: gdi\enumdisplaymonitors.htm
old-project: gdi
ms.assetid: a7668c28-77c9-4373-ae1a-eab3cb98f866
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: EnumDisplayMonitors, EnumDisplayMonitors function [Windows GDI], _win32_EnumDisplayMonitors, gdi.enumdisplaymonitors, winuser/EnumDisplayMonitors
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
-	Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
-	minuser.dll
-	api-ms-win-ntuser-sysparams-l1-1-0.dll
-	Ext-MS-Win-NTUser-SysParams-Ext-L1-1-0.dll
api_name:
-	EnumDisplayMonitors
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumDisplayMonitors function


## -description


The <b>EnumDisplayMonitors</b> function enumerates display monitors (including invisible pseudo-monitors associated with the mirroring drivers) that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context. <b>EnumDisplayMonitors</b> calls an application-defined <a href="https://msdn.microsoft.com/2d69e363-2b2c-450f-9069-488b80991217">MonitorEnumProc</a> callback function once for each monitor that is enumerated. Note that <a href="base.getsystemmetrics">GetSystemMetrics</a> (SM_CMONITORS) counts only the display monitors.


## -parameters




### -param hdc [in]

A handle to a display device context that defines the visible region of interest.

If this parameter is <b>NULL</b>, the <i>hdcMonitor</i> parameter passed to the callback function will be <b>NULL</b>, and the visible region of interest is the virtual screen that encompasses all the displays on the desktop.


### -param lprcClip [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies a clipping rectangle. The region of interest is the intersection of the clipping rectangle with the visible region specified by <i>hdc</i>.

If <i>hdc</i> is non-<b>NULL</b>, the coordinates of the clipping rectangle are relative to the origin of the <i>hdc</i>. If <i>hdc</i> is <b>NULL</b>, the coordinates are virtual-screen coordinates.

This parameter can be <b>NULL</b> if you don't want to clip the region specified by <i>hdc</i>.


### -param lpfnEnum [in]

A pointer to a <a href="https://msdn.microsoft.com/2d69e363-2b2c-450f-9069-488b80991217">MonitorEnumProc</a> application-defined callback function.


### -param dwData [in]

Application-defined data that <b>EnumDisplayMonitors</b> passes directly to the <a href="https://msdn.microsoft.com/2d69e363-2b2c-450f-9069-488b80991217">MonitorEnumProc</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



There are two reasons to call the <b>EnumDisplayMonitors</b> function:

<ul>
<li>You want to draw optimally into a device context that spans several display monitors, and the monitors have different color formats.</li>
<li>You want to obtain a handle and position rectangle for one or more display monitors.</li>
</ul>
To determine whether all the display monitors in a system share the same color format, call <a href="base.getsystemmetrics">GetSystemMetrics</a> (SM_SAMEDISPLAYFORMAT).

You do not need to use the <b>EnumDisplayMonitors</b> function when a window spans display monitors that have different color formats. You can continue to paint under the assumption that the entire screen has the color properties of the primary monitor. Your windows will look fine. <b>EnumDisplayMonitors</b> just lets you make them look better.

Setting the <i>hdc</i> parameter to <b>NULL</b> lets you use the <b>EnumDisplayMonitors</b> function to obtain a handle and position rectangle for one or more display monitors. The following table shows how the four combinations of <b>NULL</b> and non-<b>NULL</b><i>hdc</i> and <i>lprcClip</i> values affect the behavior of the <b>EnumDisplayMonitors</b> function.

<table>
<tr>
<th><i>hdc</i></th>
<th><i>lprcRect</i></th>
<th>EnumDisplayMonitors behavior</th>
</tr>
<tr>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
<td>Enumerates all display monitors.The callback function receives a <b>NULL</b> HDC.

</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>non-<b>NULL</b></td>
<td>Enumerates all display monitors that intersect the clipping rectangle. Use virtual screen coordinates for the clipping rectangle.The callback function receives a <b>NULL</b> HDC.

</td>
</tr>
<tr>
<td>non-<b>NULL</b></td>
<td><b>NULL</b></td>
<td>Enumerates all display monitors that intersect the visible region of the device context.The callback function receives a handle to a DC for the specific display monitor.

</td>
</tr>
<tr>
<td>non-<b>NULL</b></td>
<td>non-<b>NULL</b></td>
<td>Enumerates all display monitors that intersect the visible region of the device context and the clipping rectangle. Use device context coordinates for the clipping rectangle.The callback function receives a handle to a DC for the specific display monitor.

</td>
</tr>
</table>
 


#### Examples

To paint in response to a WM_PAINT message, using the capabilities of each monitor, you can use code like this in a window procedure:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
case WM_PAINT:
  hdc = BeginPaint(hwnd, &amp;ps);
  EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
  EndPaint(hwnd, &amp;ps);
</pre>
</td>
</tr>
</table></span></div>
To paint the top half of a window using the capabilities of each monitor, you can use code like this:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
GetClientRect(hwnd, &amp;rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &amp;rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
</pre>
</td>
</tr>
</table></span></div>
To paint the entire virtual screen optimally for each display monitor, you can use code like this:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
</pre>
</td>
</tr>
</table></span></div>
To retrieve information about all of the display monitors, use code like this:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="base.getsystemmetrics">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/2d69e363-2b2c-450f-9069-488b80991217">MonitorEnumProc</a>



<a href="https://msdn.microsoft.com/a64b256c-e7a1-4ee2-a346-4b7abcab9e90">Multiple Display Monitors Functions</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>
 

 

