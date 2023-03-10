---
UID: NF:shobjidl_core.IDesktopWallpaper.SetSlideshow
title: IDesktopWallpaper::SetSlideshow (shobjidl_core.h)
description: Specifies the images to use for the desktop wallpaper slideshow.
helpviewer_keywords: ["IDesktopWallpaper interface [Windows Shell]","SetSlideshow method","IDesktopWallpaper.SetSlideshow","IDesktopWallpaper::SetSlideshow","SetSlideshow","SetSlideshow method [Windows Shell]","SetSlideshow method [Windows Shell]","IDesktopWallpaper interface","shell.IDesktopWallpaper_SetSlideshow","shobjidl_core/IDesktopWallpaper::SetSlideshow"]
old-location: shell\IDesktopWallpaper_SetSlideshow.htm
tech.root: shell
ms.assetid: 0E4743A0-75AB-456a-BAAE-8EC4C0D14E6C
ms.date: 12/05/2018
ms.keywords: IDesktopWallpaper interface [Windows Shell],SetSlideshow method, IDesktopWallpaper.SetSlideshow, IDesktopWallpaper::SetSlideshow, SetSlideshow, SetSlideshow method [Windows Shell], SetSlideshow method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetSlideshow, shobjidl_core/IDesktopWallpaper::SetSlideshow
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
 - IDesktopWallpaper::SetSlideshow
 - shobjidl_core/IDesktopWallpaper::SetSlideshow
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
 - IDesktopWallpaper.SetSlideshow
---

# IDesktopWallpaper::SetSlideshow


## -description

Specifies the images to use for the desktop wallpaper slideshow.

## -parameters

### -param items [in]

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a> that contains the slideshow images. This array can contain individual items stored in the same container (files stored in a folder), or it can contain a single item which is the container itself (a folder that contains images). Any other configuration of the array will cause this method to fail.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getslideshow">IDesktopWallpaper::GetSlideshow</a>