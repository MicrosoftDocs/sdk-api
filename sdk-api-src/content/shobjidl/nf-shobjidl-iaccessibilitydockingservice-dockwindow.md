---
UID: NF:shobjidl.IAccessibilityDockingService.DockWindow
title: IAccessibilityDockingService::DockWindow (shobjidl.h)
description: Docks the specified window handle to the specified monitor handle.
helpviewer_keywords: ["DockWindow","DockWindow method [COM]","DockWindow method [COM]","IAccessibilityDockingService interface","IAccessibilityDockingService interface [COM]","DockWindow method","IAccessibilityDockingService.DockWindow","IAccessibilityDockingService::DockWindow","com.iaccessibilitydockingservice_dockwindow","shobjidl/IAccessibilityDockingService::DockWindow"]
old-location: com\iaccessibilitydockingservice_dockwindow.htm
tech.root: com
ms.assetid: 99C6A82C-A421-4A5E-B23A-167384A7AB90
ms.date: 12/05/2018
ms.keywords: DockWindow, DockWindow method [COM], DockWindow method [COM],IAccessibilityDockingService interface, IAccessibilityDockingService interface [COM],DockWindow method, IAccessibilityDockingService.DockWindow, IAccessibilityDockingService::DockWindow, com.iaccessibilitydockingservice_dockwindow, shobjidl/IAccessibilityDockingService::DockWindow
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessibilityDockingService::DockWindow
 - shobjidl/IAccessibilityDockingService::DockWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl.h
api_name:
 - IAccessibilityDockingService.DockWindow
---

# IAccessibilityDockingService::DockWindow


## -description

Docks the specified window handle to the specified monitor handle.

## -parameters

### -param hwnd [in]

The accessibility application window that will be docked on the passed monitor handle.

### -param hMonitor [in]

The monitor on which the accessibility application window will be docked.

### -param cyRequested

TBD

### -param pCallback [in]

The callback pointer on which the accessibility application will receive the <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservice-undockwindow">Undock</a> notification.


#### - uHeight [in]

The height at which the window will be docked, in pixels, if this function is successful. Must be less than or equal to the <i>puMaxHeight</i> variable retrieved from a call to the <a href="/windows/desktop/com/iaccessibilitydockingservice-getavailablesize">GetAvailableSize</a> method.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The window handle or monitor handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process is not a UIAcess accessibility application or the calling process does not own the window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMM_E_DOCKOCCUPIED</b></dt>
</dl>
</td>
<td width="60%">
There is already another window occupying the docking space. Only one window can be docked at a time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMM_E_INSUFFICIENTHEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The requested <i>uHeight</i> is larger than the maximum allowed docking height for the specified monitor. However, if this error code is being returned, it means that this monitor does support docking, though at a height indicated by a call to the <a href="/windows/desktop/com/iaccessibilitydockingservice-getavailablesize">GetAvailableSize</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_MONITOR_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The monitor specified by the monitor handle does not support docking.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice">IAccessibilityDockingService</a>