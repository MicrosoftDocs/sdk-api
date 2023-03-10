---
UID: NF:shobjidl_core.IDesktopWallpaper.SetSlideshowOptions
title: IDesktopWallpaper::SetSlideshowOptions (shobjidl_core.h)
description: Sets the desktop wallpaper slideshow settings for shuffle and timing.
helpviewer_keywords: ["DSO_SHUFFLEIMAGES","IDesktopWallpaper interface [Windows Shell]","SetSlideshowOptions method","IDesktopWallpaper.SetSlideshowOptions","IDesktopWallpaper::SetSlideshowOptions","SetSlideshowOptions","SetSlideshowOptions method [Windows Shell]","SetSlideshowOptions method [Windows Shell]","IDesktopWallpaper interface","shell.IDesktopWallpaper_SetSlideshowOptions","shobjidl_core/IDesktopWallpaper::SetSlideshowOptions"]
old-location: shell\IDesktopWallpaper_SetSlideshowOptions.htm
tech.root: shell
ms.assetid: B3106354-C321-4770-834F-D2EF790AE114
ms.date: 12/05/2018
ms.keywords: DSO_SHUFFLEIMAGES, IDesktopWallpaper interface [Windows Shell],SetSlideshowOptions method, IDesktopWallpaper.SetSlideshowOptions, IDesktopWallpaper::SetSlideshowOptions, SetSlideshowOptions, SetSlideshowOptions method [Windows Shell], SetSlideshowOptions method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetSlideshowOptions, shobjidl_core/IDesktopWallpaper::SetSlideshowOptions
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
 - IDesktopWallpaper::SetSlideshowOptions
 - shobjidl_core/IDesktopWallpaper::SetSlideshowOptions
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
 - IDesktopWallpaper.SetSlideshowOptions
---

# IDesktopWallpaper::SetSlideshowOptions


## -description

Sets the desktop wallpaper slideshow settings for shuffle and timing.

## -parameters

### -param options [in]

Set to either 0 to disable shuffle or the following value.



#### DSO_SHUFFLEIMAGES (0x01)

Enable shuffle; advance through the slideshow in a random order.

### -param slideshowTick [in]

The amount of time, in milliseconds, between image transitions.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getslideshowoptions">IDesktopWallpaper::GetSlideshowOptions</a>