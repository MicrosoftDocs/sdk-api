---
UID: NF:shobjidl_core.IDesktopWallpaper.GetMonitorDevicePathCount
title: IDesktopWallpaper::GetMonitorDevicePathCount (shobjidl_core.h)
description: Retrieves the number of monitors that are associated with the system.
helpviewer_keywords: ["GetMonitorDevicePathCount","GetMonitorDevicePathCount method [Windows Shell]","GetMonitorDevicePathCount method [Windows Shell]","IDesktopWallpaper interface","IDesktopWallpaper interface [Windows Shell]","GetMonitorDevicePathCount method","IDesktopWallpaper.GetMonitorDevicePathCount","IDesktopWallpaper::GetMonitorDevicePathCount","shell.IDesktopWallpaper_GetMonitorDevicePathCount","shobjidl_core/IDesktopWallpaper::GetMonitorDevicePathCount"]
old-location: shell\IDesktopWallpaper_GetMonitorDevicePathCount.htm
tech.root: shell
ms.assetid: E7490E24-7BCE-4fbb-8512-998EAE045CE7
ms.date: 12/05/2018
ms.keywords: GetMonitorDevicePathCount, GetMonitorDevicePathCount method [Windows Shell], GetMonitorDevicePathCount method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetMonitorDevicePathCount method, IDesktopWallpaper.GetMonitorDevicePathCount, IDesktopWallpaper::GetMonitorDevicePathCount, shell.IDesktopWallpaper_GetMonitorDevicePathCount, shobjidl_core/IDesktopWallpaper::GetMonitorDevicePathCount
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
 - IDesktopWallpaper::GetMonitorDevicePathCount
 - shobjidl_core/IDesktopWallpaper::GetMonitorDevicePathCount
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
 - IDesktopWallpaper.GetMonitorDevicePathCount
---

# IDesktopWallpaper::GetMonitorDevicePathCount


## -description

Retrieves the number of monitors that are associated with the system.

## -parameters

### -param count [out]

A pointer to a value that, when this method returns successfully, receives the number of monitors.

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

The count retrieved through this method includes monitors that are currently detached but that have an image assigned to them. Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitorrect">GetMonitorRECT</a> to distinguish between attached and detached monitors.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathat">IDesktopWallpaper::GetMonitorDevicePathAt</a>