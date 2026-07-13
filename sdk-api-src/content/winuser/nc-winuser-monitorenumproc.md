---
UID: NC:winuser.MONITORENUMPROC
title: MONITORENUMPROC (winuser.h)
description: A MonitorEnumProc function is an application-defined callback function that is called by the EnumDisplayMonitors function.
helpviewer_keywords: ["MonitorEnumProc","MonitorEnumProc callback","MonitorEnumProc callback function [Windows GDI]","_win32_MonitorEnumProc","gdi.monitorenumproc","winuser/MonitorEnumProc"]
old-location: gdi\monitorenumproc.htm
tech.root: gdi
ms.assetid: 2d69e363-2b2c-450f-9069-488b80991217
ms.date: 09/30/2025
ms.keywords: MonitorEnumProc, MonitorEnumProc callback, MonitorEnumProc callback function [Windows GDI], _win32_MonitorEnumProc, gdi.monitorenumproc, winuser/MonitorEnumProc
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
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
 - MONITORENUMPROC
 - winuser/MONITORENUMPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - MonitorEnumProc
---

# MONITORENUMPROC callback function

## -description

An application-defined callback function used with the [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) function. The **MONITORENUMPROC** type defines a pointer to this callback function. _MonitorEnumProc_ is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: **HMONITOR**

A handle to the display monitor. This value will always be non-**NULL**. This parameter is typically named _hMonitor_.

### -param unnamedParam2

Type: **HDC**

A handle to a device context. This parameter is typically named _hdcMonitor_.

The device context has color attributes that are appropriate for the display monitor identified by _hMonitor_. The clipping area of the device context is set to the intersection of the visible region of the device context identified by the _hdc_ parameter of [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors), the rectangle pointed to by the _lprcClip_ parameter of **EnumDisplayMonitors**, and the display monitor rectangle.

This value is **NULL** if the _hdc_ parameter of [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) was **NULL**.

### -param unnamedParam3

Type: **LPRECT**

A pointer to a [RECT](/windows/desktop/api/windef/ns-windef-rect) structure. This parameter is typically named _lprcMonitor_.

If _hdcMonitor_ is non-**NULL**, this rectangle is the intersection of the clipping area of the device context identified by _hdcMonitor_ and the display monitor rectangle. The rectangle coordinates are device-context coordinates.

If _hdcMonitor_ is **NULL**, this rectangle is the display monitor rectangle. The rectangle coordinates are virtual-screen coordinates.

### -param unnamedParam4

Type: **LPARAM**

Application-defined data that [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) passes directly to the enumeration function. This parameter is typically named _dwData_.

## -returns

Type: **BOOL**

To continue the enumeration, return **TRUE**.

To stop the enumeration, return **FALSE**.

## -remarks

> [!NOTE]
> The parameters are defined in the header with no names: `typedef BOOL (CALLBACK* MONITORENUMPROC)(HMONITOR, HDC, LPRECT, LPARAM);`. Therefore, the syntax block lists them as `unnamedParam1` - `unnamedParam4`. You can name these parameters anything in your app. However, they are usually named as shown in the parameter descriptions.

You can use the [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) function to enumerate the set of display monitors that intersect the visible region of a specified device context and, optionally, a clipping rectangle. To do this, set the _hdc_ parameter to a non-**NULL** value, and set the _lprcClip_ parameter as needed.

You can also use the [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) function to enumerate one or more of the display monitors on the desktop, without supplying a device context. To do this, set the _hdc_ parameter of **EnumDisplayMonitors** to **NULL** and set the _lprcClip_ parameter as needed.

In all cases, [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) calls a specified _MonitorEnumProc_ function once for each display monitor in the calculated enumeration set. The _MonitorEnumProc_ function always receives a handle to the display monitor.

If the _hdc_ parameter of [EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) is non-**NULL**, the _MonitorEnumProc_ function also receives a handle to a device context whose color format is appropriate for the display monitor. You can then paint into the device context in a manner that is optimal for the display monitor.

## -see-also

[EnumDisplayMonitors](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors)

[Multiple Display Monitors Functions](/windows/desktop/gdi/multiple-display-monitors-functions)

[Multiple Display Monitors Overview](/windows/desktop/gdi/multiple-display-monitors)
