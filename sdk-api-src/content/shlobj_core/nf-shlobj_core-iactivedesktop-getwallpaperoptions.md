---
UID: NF:shlobj_core.IActiveDesktop.GetWallpaperOptions
title: IActiveDesktop::GetWallpaperOptions
author: windows-sdk-content
description: Gets the wallpaper options.
old-location: lwef\iactivedesktop_getwallpaperoptions.htm
tech.root: lwef
ms.assetid: b524a2b8-e6b6-4592-9435-88a6842b2338
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetWallpaperOptions, GetWallpaperOptions method [Legacy Windows Environment Features], GetWallpaperOptions method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetWallpaperOptions method, IActiveDesktop.GetWallpaperOptions, IActiveDesktop::GetWallpaperOptions, _win32_IActiveDesktop_GetWallpaperOptions, lwef.iactivedesktop_getwallpaperoptions, shell.iactivedesktop_getwallpaperoptions, shlobj_core/IActiveDesktop::GetWallpaperOptions
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
 - IActiveDesktop.GetWallpaperOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::GetWallpaperOptions


## -description


Gets the wallpaper options.


## -parameters




### -param pwpo [in, out]

Type: <b>LPWALLPAPEROPT</b>

The address of a <a href="https://msdn.microsoft.com/5fafbc3a-606c-4175-ac3a-132a1bfded07">WALLPAPEROPT</a> structure containing the options currently set. 


### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

