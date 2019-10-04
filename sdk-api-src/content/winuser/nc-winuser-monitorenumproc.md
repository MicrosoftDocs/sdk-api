---
UID: NC:winuser.MONITORENUMPROC
title: MONITORENUMPROC (winuser.h)
author: windows-sdk-content
description: A MonitorEnumProc function is an application-defined callback function that is called by the EnumDisplayMonitors function.
old-location: gdi\monitorenumproc.htm
tech.root: gdi
ms.assetid: 2d69e363-2b2c-450f-9069-488b80991217
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MonitorEnumProc, MonitorEnumProc callback, MonitorEnumProc callback function [Windows GDI], _win32_MonitorEnumProc, gdi.monitorenumproc, winuser/MonitorEnumProc
ms.topic: callback
f1_keywords: 
 - "winuser/MonitorEnumProc"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - MonitorEnumProc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MONITORENUMPROC callback function


## -description


A <b>MonitorEnumProc</b> function is an application-defined callback function that is called by the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> function.

A value of type <b>MONITORENUMPROC</b> is a pointer to a <b>MonitorEnumProc</b> function.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - dwData [in]

Application-defined data that <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> passes directly to the enumeration function.


#### - hMonitor [in]

A handle to the display monitor. This value will always be non-<b>NULL</b>.


#### - hdcMonitor [in]

A handle to a device context.

The device context has color attributes that are appropriate for the display monitor identified by <i>hMonitor</i>. The clipping area of the device context is set to the intersection of the visible region of the device context identified by the <i>hdc</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a>, the rectangle pointed to by the <i>lprcClip</i> parameter of <b>EnumDisplayMonitors</b>, and the display monitor rectangle.

This value is <b>NULL</b> if the <i>hdc</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> was <b>NULL</b>.


#### - lprcMonitor [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure.

If <i>hdcMonitor</i> is non-<b>NULL</b>, this rectangle is the intersection of the clipping area of the device context identified by <i>hdcMonitor</i> and the display monitor rectangle. The rectangle coordinates are device-context coordinates.

If <i>hdcMonitor</i> is <b>NULL</b>, this rectangle is the display monitor rectangle. The rectangle coordinates are virtual-screen coordinates.


## -returns



To continue the enumeration, return <b>TRUE</b>.

To stop the enumeration, return <b>FALSE</b>.




## -remarks



You can use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> function to enumerate the set of display monitors that intersect the visible region of a specified device context and, optionally, a clipping rectangle. To do this, set the <i>hdc</i> parameter to a non-<b>NULL</b> value, and set the <i>lprcClip</i> parameter as needed.

You can also use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> function to enumerate one or more of the display monitors on the desktop, without supplying a device context. To do this, set the <i>hdc</i> parameter of <b>EnumDisplayMonitors</b> to <b>NULL</b> and set the <i>lprcClip</i> parameter as needed.

In all cases, <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> calls a specified <b>MonitorEnumProc</b> function once for each display monitor in the calculated enumeration set. The <b>MonitorEnumProc</b> function always receives a handle to the display monitor.

If the <i>hdc</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> is non-<b>NULL</b>, the <b>MonitorEnumProc</b> function also receives a handle to a device context whose color format is appropriate for the display monitor. You can then paint into the device context in a manner that is optimal for the display monitor.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/multiple-display-monitors-functions">Multiple Display Monitors Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors Overview</a>
 

 

