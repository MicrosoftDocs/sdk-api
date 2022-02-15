---
UID: NF:shlobj_core.IActiveDesktop.GetWallpaperOptions
title: IActiveDesktop::GetWallpaperOptions (shlobj_core.h)
description: Gets the wallpaper options.
helpviewer_keywords: ["GetWallpaperOptions","GetWallpaperOptions method [Legacy Windows Environment Features]","GetWallpaperOptions method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","GetWallpaperOptions method","IActiveDesktop.GetWallpaperOptions","IActiveDesktop::GetWallpaperOptions","_win32_IActiveDesktop_GetWallpaperOptions","lwef.iactivedesktop_getwallpaperoptions","shell.iactivedesktop_getwallpaperoptions","shlobj_core/IActiveDesktop::GetWallpaperOptions"]
old-location: lwef\iactivedesktop_getwallpaperoptions.htm
tech.root: lwef
ms.assetid: b524a2b8-e6b6-4592-9435-88a6842b2338
ms.date: 12/05/2018
ms.keywords: GetWallpaperOptions, GetWallpaperOptions method [Legacy Windows Environment Features], GetWallpaperOptions method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetWallpaperOptions method, IActiveDesktop.GetWallpaperOptions, IActiveDesktop::GetWallpaperOptions, _win32_IActiveDesktop_GetWallpaperOptions, lwef.iactivedesktop_getwallpaperoptions, shell.iactivedesktop_getwallpaperoptions, shlobj_core/IActiveDesktop::GetWallpaperOptions
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveDesktop::GetWallpaperOptions
 - shlobj_core/IActiveDesktop::GetWallpaperOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop.GetWallpaperOptions
---

# IActiveDesktop::GetWallpaperOptions


## -description

Gets the wallpaper options.

## -parameters

### -param pwpo [in, out]

Type: <b>LPWALLPAPEROPT</b>

The address of a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-wallpaperopt">WALLPAPEROPT</a> structure containing the options currently set.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>