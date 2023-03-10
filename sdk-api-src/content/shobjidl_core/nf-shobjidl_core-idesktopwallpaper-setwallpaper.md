---
UID: NF:shobjidl_core.IDesktopWallpaper.SetWallpaper
title: IDesktopWallpaper::SetWallpaper (shobjidl_core.h)
description: Sets the desktop wallpaper.
helpviewer_keywords: ["IDesktopWallpaper interface [Windows Shell]","SetWallpaper method","IDesktopWallpaper.SetWallpaper","IDesktopWallpaper::SetWallpaper","SetWallpaper","SetWallpaper method [Windows Shell]","SetWallpaper method [Windows Shell]","IDesktopWallpaper interface","shell.IDesktopWallpaper_SetWallpaper","shobjidl_core/IDesktopWallpaper::SetWallpaper"]
old-location: shell\IDesktopWallpaper_SetWallpaper.htm
tech.root: shell
ms.assetid: 5E0731DC-8B70-40dc-B90A-97B1E3E4D55D
ms.date: 12/05/2018
ms.keywords: IDesktopWallpaper interface [Windows Shell],SetWallpaper method, IDesktopWallpaper.SetWallpaper, IDesktopWallpaper::SetWallpaper, SetWallpaper, SetWallpaper method [Windows Shell], SetWallpaper method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetWallpaper, shobjidl_core/IDesktopWallpaper::SetWallpaper
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
 - IDesktopWallpaper::SetWallpaper
 - shobjidl_core/IDesktopWallpaper::SetWallpaper
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
 - IDesktopWallpaper.SetWallpaper
---

# IDesktopWallpaper::SetWallpaper


## -description

Sets the desktop wallpaper.

## -parameters

### -param monitorID [in]

The ID of the monitor. This value can be obtained through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathat">GetMonitorDevicePathAt</a>. Set this value to NULL to set the wallpaper image on all monitors.

### -param wallpaper [in]

The full path of the wallpaper image file.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getwallpaper">IDesktopWallpaper::GetWallpaper</a>