---
UID: NF:shlobj_core.IActiveDesktop.GetWallpaper
title: IActiveDesktop::GetWallpaper
author: windows-sdk-content
description: Gets the current wallpaper.
old-location: lwef\iactivedesktop_getwallpaper.htm
tech.root: lwef
ms.assetid: b56cf857-5f3c-47f0-a1c2-e578c44c971b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AD_GETWP_BMP, AD_GETWP_IMAGE, AD_GETWP_LAST_APPLIED, GetWallpaper, GetWallpaper method [Legacy Windows Environment Features], GetWallpaper method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetWallpaper method, IActiveDesktop.GetWallpaper, IActiveDesktop::GetWallpaper, _win32_IActiveDesktop_GetWallpaper, lwef.iactivedesktop_getwallpaper, shell.iactivedesktop_getwallpaper, shlobj_core/IActiveDesktop::GetWallpaper
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop.GetWallpaper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shlobj_core.h
: 
- IActiveDesktop.GetWallpaper
: 
---

# IActiveDesktop::GetWallpaper


## -description


Gets the current wallpaper.


## -parameters




### -param pwszWallpaper [out]

Type: <b>PWSTR</b>

When this method returns, contains a pointer to a null-terminated, Unicode buffer that contains the file name of the wallpaper.


### -param cchWallpaper

Type: <b>UINT</b>

The size of the <i>pwszWallpaper</i> string, in characters.


### -param dwFlags

Type: <b>DWORD</b>

The type of wallpaper to get. One of the following values.



#### AD_GETWP_BMP (0x00000000)

Get a bitmap.



#### AD_GETWP_IMAGE (0x00000001)

Get an image.



#### AD_GETWP_LAST_APPLIED (0x00000002)

Get the type of wallpaper that was last applied.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



