---
UID: NF:shlobj_core.IActiveDesktop.SetWallpaper
title: IActiveDesktop::SetWallpaper (shlobj_core.h)
description: Sets the wallpaper for the Active Desktop.
helpviewer_keywords: ["IActiveDesktop interface [Legacy Windows Environment Features]","SetWallpaper method","IActiveDesktop.SetWallpaper","IActiveDesktop::SetWallpaper","SetWallpaper","SetWallpaper method [Legacy Windows Environment Features]","SetWallpaper method [Legacy Windows Environment Features]","IActiveDesktop interface","_win32_IActiveDesktop_SetWallpaper","lwef.iactivedesktop_setwallpaper","shell.iactivedesktop_setwallpaper","shlobj_core/IActiveDesktop::SetWallpaper"]
old-location: lwef\iactivedesktop_setwallpaper.htm
tech.root: lwef
ms.assetid: e789a8f1-3e65-4fa7-a62b-8fad6114ed46
ms.date: 12/05/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],SetWallpaper method, IActiveDesktop.SetWallpaper, IActiveDesktop::SetWallpaper, SetWallpaper, SetWallpaper method [Legacy Windows Environment Features], SetWallpaper method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_SetWallpaper, lwef.iactivedesktop_setwallpaper, shell.iactivedesktop_setwallpaper, shlobj_core/IActiveDesktop::SetWallpaper
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
 - IActiveDesktop::SetWallpaper
 - shlobj_core/IActiveDesktop::SetWallpaper
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
 - IActiveDesktop.SetWallpaper
---

# IActiveDesktop::SetWallpaper


## -description

Sets the wallpaper for the Active Desktop.

## -parameters

### -param pwszWallpaper [in]

Type: <b>PCWSTR</b>

A string value containing the file name of the wallpaper to be set.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>