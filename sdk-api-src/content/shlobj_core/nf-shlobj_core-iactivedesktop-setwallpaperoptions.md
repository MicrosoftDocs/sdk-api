---
UID: NF:shlobj_core.IActiveDesktop.SetWallpaperOptions
title: IActiveDesktop::SetWallpaperOptions (shlobj_core.h)
author: windows-sdk-content
description: Sets the wallpaper options.
old-location: lwef\iactivedesktop_setwallpaperoptions.htm
tech.root: lwef
ms.assetid: dbe09c68-26f8-4db4-9e74-87f0a94c7918
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],SetWallpaperOptions method, IActiveDesktop.SetWallpaperOptions, IActiveDesktop::SetWallpaperOptions, SetWallpaperOptions, SetWallpaperOptions method [Legacy Windows Environment Features], SetWallpaperOptions method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_SetWallpaperOptions, lwef.iactivedesktop_setwallpaperoptions, shell.iactivedesktop_setwallpaperoptions, shlobj_core/IActiveDesktop::SetWallpaperOptions
ms.topic: method
f1_keywords: ["shlobj_core/IActiveDesktop.SetWallpaperOptions"]
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
ms.custom: 19H1
---

# IActiveDesktop::SetWallpaperOptions


## -description


Sets the wallpaper options.


## -parameters




### -param pwpo [in]

Type: <b>LPCWALLPAPEROPT</b>

The address of the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-_tagwallpaperopt">WALLPAPEROPT</a> structure containing the options to be set. 


### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>
 

 

