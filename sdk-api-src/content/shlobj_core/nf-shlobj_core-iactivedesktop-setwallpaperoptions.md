---
UID: NF:shlobj_core.IActiveDesktop.SetWallpaperOptions
title: IActiveDesktop::SetWallpaperOptions
author: windows-sdk-content
description: Sets the wallpaper options.
old-location: lwef\iactivedesktop_setwallpaperoptions.htm
tech.root: lwef
ms.assetid: dbe09c68-26f8-4db4-9e74-87f0a94c7918
ms.author: windowssdkdev
ms.date: 10/31/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],SetWallpaperOptions method, IActiveDesktop.SetWallpaperOptions, IActiveDesktop::SetWallpaperOptions, SetWallpaperOptions, SetWallpaperOptions method [Legacy Windows Environment Features], SetWallpaperOptions method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_SetWallpaperOptions, lwef.iactivedesktop_setwallpaperoptions, shell.iactivedesktop_setwallpaperoptions, shlobj_core/IActiveDesktop::SetWallpaperOptions
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
 - IActiveDesktop.SetWallpaperOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::SetWallpaperOptions


## -description


Sets the wallpaper options.


## -parameters




### -param pwpo [in]

Type: <b>LPCWALLPAPEROPT</b>

The address of the <a href="https://msdn.microsoft.com/5fafbc3a-606c-4175-ac3a-132a1bfded07">WALLPAPEROPT</a> structure containing the options to be set. 


### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

