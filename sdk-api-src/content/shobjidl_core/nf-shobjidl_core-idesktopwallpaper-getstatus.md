---
UID: NF:shobjidl_core.IDesktopWallpaper.GetStatus
title: IDesktopWallpaper::GetStatus (shobjidl_core.h)
description: Gets the current status of the slideshow.
helpviewer_keywords: ["DSS_DISABLED_BY_REMOTE_SESSION","DSS_ENABLED","DSS_SLIDESHOW","GetStatus","GetStatus method [Windows Shell]","GetStatus method [Windows Shell]","IDesktopWallpaper interface","IDesktopWallpaper interface [Windows Shell]","GetStatus method","IDesktopWallpaper.GetStatus","IDesktopWallpaper::GetStatus","shell.IDesktopWallpaper_GetStatus","shobjidl_core/IDesktopWallpaper::GetStatus"]
old-location: shell\IDesktopWallpaper_GetStatus.htm
tech.root: shell
ms.assetid: 19F2776E-0B5F-45c9-962A-08BFC0273066
ms.date: 12/05/2018
ms.keywords: DSS_DISABLED_BY_REMOTE_SESSION, DSS_ENABLED, DSS_SLIDESHOW, GetStatus, GetStatus method [Windows Shell], GetStatus method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetStatus method, IDesktopWallpaper.GetStatus, IDesktopWallpaper::GetStatus, shell.IDesktopWallpaper_GetStatus, shobjidl_core/IDesktopWallpaper::GetStatus
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
 - IDesktopWallpaper::GetStatus
 - shobjidl_core/IDesktopWallpaper::GetStatus
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
 - IDesktopWallpaper.GetStatus
---

# IDesktopWallpaper::GetStatus


## -description

Gets the current status of the slideshow.

## -parameters

### -param state [out]

A pointer to a DESKTOP_SLIDESHOW_STATE value that, when this method returns successfully, receives one or more of the following flags.



#### DSS_ENABLED (0x01)

Slideshows are enabled.



#### DSS_SLIDESHOW (0x02)

A slideshow is currently configured.



#### DSS_DISABLED_BY_REMOTE_SESSION (0x04)

A remote session has temporarily disabled the slideshow.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>