---
UID: NF:shobjidl_core.IDesktopWallpaper.GetBackgroundColor
title: IDesktopWallpaper::GetBackgroundColor (shobjidl_core.h)
description: Retrieves the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.
helpviewer_keywords: ["GetBackgroundColor","GetBackgroundColor method [Windows Shell]","GetBackgroundColor method [Windows Shell]","IDesktopWallpaper interface","IDesktopWallpaper interface [Windows Shell]","GetBackgroundColor method","IDesktopWallpaper.GetBackgroundColor","IDesktopWallpaper::GetBackgroundColor","shell.IDesktopWallpaper_GetBackgroundColor","shobjidl_core/IDesktopWallpaper::GetBackgroundColor"]
old-location: shell\IDesktopWallpaper_GetBackgroundColor.htm
tech.root: shell
ms.assetid: 92666512-BE10-4ee7-B670-18F0C714A4C9
ms.date: 12/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [Windows Shell], GetBackgroundColor method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetBackgroundColor method, IDesktopWallpaper.GetBackgroundColor, IDesktopWallpaper::GetBackgroundColor, shell.IDesktopWallpaper_GetBackgroundColor, shobjidl_core/IDesktopWallpaper::GetBackgroundColor
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
 - IDesktopWallpaper::GetBackgroundColor
 - shobjidl_core/IDesktopWallpaper::GetBackgroundColor
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
 - IDesktopWallpaper.GetBackgroundColor
---

# IDesktopWallpaper::GetBackgroundColor


## -description

Retrieves the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.

## -parameters

### -param color [out]

A pointer to a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that, when this method returns successfully, receives the RGB color value. If this method fails, this value is set to 0.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setbackgroundcolor">IDesktopWallpaper::SetBackgroundColor</a>