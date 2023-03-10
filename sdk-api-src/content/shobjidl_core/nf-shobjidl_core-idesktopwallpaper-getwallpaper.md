---
UID: NF:shobjidl_core.IDesktopWallpaper.GetWallpaper
title: IDesktopWallpaper::GetWallpaper (shobjidl_core.h)
description: Gets the current desktop wallpaper.
helpviewer_keywords: ["GetWallpaper","GetWallpaper method [Windows Shell]","GetWallpaper method [Windows Shell]","IDesktopWallpaper interface","IDesktopWallpaper interface [Windows Shell]","GetWallpaper method","IDesktopWallpaper.GetWallpaper","IDesktopWallpaper::GetWallpaper","shell.IDesktopWallpaper_GetWallpaper","shobjidl_core/IDesktopWallpaper::GetWallpaper"]
old-location: shell\IDesktopWallpaper_GetWallpaper.htm
tech.root: shell
ms.assetid: A5AC5EB3-2091-4547-8B6A-C60C4E90DFBC
ms.date: 12/05/2018
ms.keywords: GetWallpaper, GetWallpaper method [Windows Shell], GetWallpaper method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetWallpaper method, IDesktopWallpaper.GetWallpaper, IDesktopWallpaper::GetWallpaper, shell.IDesktopWallpaper_GetWallpaper, shobjidl_core/IDesktopWallpaper::GetWallpaper
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
 - IDesktopWallpaper::GetWallpaper
 - shobjidl_core/IDesktopWallpaper::GetWallpaper
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
 - IDesktopWallpaper.GetWallpaper
---

# IDesktopWallpaper::GetWallpaper


## -description

Gets the current desktop wallpaper.

## -parameters

### -param monitorID [in]

The ID of the monitor. This value can be obtained through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathat">GetMonitorDevicePathAt</a>.

This value can be set to <b>NULL</b>. In that case, if a single wallpaper image is displayed on all of the system's monitors, the method returns successfully. If this value is set to <b>NULL</b> and different monitors are displaying different wallpapers or a slideshow is running, the method returns S_FALSE and an empty string in the <i>wallpaper</i> parameter.

### -param wallpaper [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the path to the wallpaper image file. Note that this image could be currently displayed on all of the system's monitors, not just the monitor specified in the <i>monitorID</i> parameter.

This string will be empty if no wallpaper image is being displayed or if a monitor is displaying a solid color. The string will also be empty if the method fails.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setwallpaper">IDesktopWallpaper::SetWallpaper</a>