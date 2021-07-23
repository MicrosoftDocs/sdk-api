---
UID: NF:shobjidl_core.IDesktopWallpaper.AdvanceSlideshow
title: IDesktopWallpaper::AdvanceSlideshow (shobjidl_core.h)
description: Switches the wallpaper on a specified monitor to the next image in the slideshow.
helpviewer_keywords: ["AdvanceSlideshow","AdvanceSlideshow method [Windows Shell]","AdvanceSlideshow method [Windows Shell]","IDesktopWallpaper interface","DSD_BACKWARD","DSD_FORWARD","IDesktopWallpaper interface [Windows Shell]","AdvanceSlideshow method","IDesktopWallpaper.AdvanceSlideshow","IDesktopWallpaper::AdvanceSlideshow","shell.IDesktopWallpaper_AdvanceSlideshow","shobjidl_core/IDesktopWallpaper::AdvanceSlideshow"]
old-location: shell\IDesktopWallpaper_AdvanceSlideshow.htm
tech.root: shell
ms.assetid: A68F6EFA-DD74-453f-A7D3-7CEC2E760FD1
ms.date: 12/05/2018
ms.keywords: AdvanceSlideshow, AdvanceSlideshow method [Windows Shell], AdvanceSlideshow method [Windows Shell],IDesktopWallpaper interface, DSD_BACKWARD, DSD_FORWARD, IDesktopWallpaper interface [Windows Shell],AdvanceSlideshow method, IDesktopWallpaper.AdvanceSlideshow, IDesktopWallpaper::AdvanceSlideshow, shell.IDesktopWallpaper_AdvanceSlideshow, shobjidl_core/IDesktopWallpaper::AdvanceSlideshow
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
 - IDesktopWallpaper::AdvanceSlideshow
 - shobjidl_core/IDesktopWallpaper::AdvanceSlideshow
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
 - IDesktopWallpaper.AdvanceSlideshow
---

# IDesktopWallpaper::AdvanceSlideshow


## -description

Switches the wallpaper on a specified monitor to the next image in the slideshow.

## -parameters

### -param monitorID [in]

The ID of the monitor on which to change the wallpaper image. This ID can be obtained through the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathat">GetMonitorDevicePathAt</a> method. If this parameter is set to <b>NULL</b>, the monitor scheduled to change next is used.

### -param direction [in]

The direction that the slideshow should advance. One of the following DESKTOP_SLIDESHOW_DIRECTION values:



#### DSD_FORWARD (0)

Advance the slideshow forward.



#### DSD_BACKWARD (1)

Advance the slideshow backward.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>