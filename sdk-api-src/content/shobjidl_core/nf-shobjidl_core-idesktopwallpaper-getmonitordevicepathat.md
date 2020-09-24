---
UID: NF:shobjidl_core.IDesktopWallpaper.GetMonitorDevicePathAt
title: IDesktopWallpaper::GetMonitorDevicePathAt (shobjidl_core.h)
description: Retrieves the unique ID of one of the system's monitors.
helpviewer_keywords: ["GetMonitorDevicePathAt","GetMonitorDevicePathAt method [Windows Shell]","GetMonitorDevicePathAt method [Windows Shell]","IDesktopWallpaper interface","IDesktopWallpaper interface [Windows Shell]","GetMonitorDevicePathAt method","IDesktopWallpaper.GetMonitorDevicePathAt","IDesktopWallpaper::GetMonitorDevicePathAt","shell.IDesktopWallpaper_GetMonitorDevicePathAt","shobjidl_core/IDesktopWallpaper::GetMonitorDevicePathAt"]
old-location: shell\IDesktopWallpaper_GetMonitorDevicePathAt.htm
tech.root: shell
ms.assetid: CE0C6B07-F9D1-4221-9D9D-8D17CF6780E6
ms.date: 12/05/2018
ms.keywords: GetMonitorDevicePathAt, GetMonitorDevicePathAt method [Windows Shell], GetMonitorDevicePathAt method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetMonitorDevicePathAt method, IDesktopWallpaper.GetMonitorDevicePathAt, IDesktopWallpaper::GetMonitorDevicePathAt, shell.IDesktopWallpaper_GetMonitorDevicePathAt, shobjidl_core/IDesktopWallpaper::GetMonitorDevicePathAt
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IDesktopWallpaper::GetMonitorDevicePathAt
 - shobjidl_core/IDesktopWallpaper::GetMonitorDevicePathAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDesktopWallpaper.GetMonitorDevicePathAt
---

# IDesktopWallpaper::GetMonitorDevicePathAt


## -description

Retrieves the unique ID of one of the system's monitors.

## -parameters

### -param monitorIndex [in]

The number of the monitor. Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathcount">GetMonitorDevicePathCount</a> to determine the total number of monitors.

### -param monitorID [out]

A pointer to the address of a buffer that, when this method returns successfully, receives the monitor's ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code, including the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided in <i>monitorID</i>.

</td>
</tr>
</table>

## -remarks

This method can be called on monitors that are currently detached but that have an image assigned to them. Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitorrect">GetMonitorRECT</a> to distinguish between attached and detached monitors.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathcount">IDesktopWallpaper::GetMonitorDevicePathCount</a>