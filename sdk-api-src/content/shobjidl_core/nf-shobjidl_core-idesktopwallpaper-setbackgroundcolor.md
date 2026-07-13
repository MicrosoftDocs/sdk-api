---
UID: NF:shobjidl_core.IDesktopWallpaper.SetBackgroundColor
title: IDesktopWallpaper::SetBackgroundColor (shobjidl_core.h)
description: Sets the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.
helpviewer_keywords: ["IDesktopWallpaper interface [Windows Shell]","SetBackgroundColor method","IDesktopWallpaper.SetBackgroundColor","IDesktopWallpaper::SetBackgroundColor","SetBackgroundColor","SetBackgroundColor method [Windows Shell]","SetBackgroundColor method [Windows Shell]","IDesktopWallpaper interface","shell.IDesktopWallpaper_SetBackgroundColor","shobjidl_core/IDesktopWallpaper::SetBackgroundColor"]
old-location: shell\IDesktopWallpaper_SetBackgroundColor.htm
tech.root: shell
ms.assetid: 9CA14C0B-4727-4702-9EB0-4D24003EB456
ms.date: 12/05/2018
ms.keywords: IDesktopWallpaper interface [Windows Shell],SetBackgroundColor method, IDesktopWallpaper.SetBackgroundColor, IDesktopWallpaper::SetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [Windows Shell], SetBackgroundColor method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetBackgroundColor, shobjidl_core/IDesktopWallpaper::SetBackgroundColor
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
 - IDesktopWallpaper::SetBackgroundColor
 - shobjidl_core/IDesktopWallpaper::SetBackgroundColor
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
 - IDesktopWallpaper.SetBackgroundColor
---

# IDesktopWallpaper::SetBackgroundColor


## -description

Sets the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.

## -parameters

### -param color [in]

A <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that specifies the background RGB color value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getbackgroundcolor">IDesktopWallpaper::GetBackgroundColor</a>