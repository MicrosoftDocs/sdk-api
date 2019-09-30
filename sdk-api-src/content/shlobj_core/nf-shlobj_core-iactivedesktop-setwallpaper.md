---
UID: NF:shlobj_core.IActiveDesktop.SetWallpaper
title: IActiveDesktop::SetWallpaper (shlobj_core.h)
author: windows-sdk-content
description: Sets the wallpaper for the Active Desktop.
old-location: lwef\iactivedesktop_setwallpaper.htm
tech.root: lwef
ms.assetid: e789a8f1-3e65-4fa7-a62b-8fad6114ed46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],SetWallpaper method, IActiveDesktop.SetWallpaper, IActiveDesktop::SetWallpaper, SetWallpaper, SetWallpaper method [Legacy Windows Environment Features], SetWallpaper method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_SetWallpaper, lwef.iactivedesktop_setwallpaper, shell.iactivedesktop_setwallpaper, shlobj_core/IActiveDesktop::SetWallpaper
ms.topic: method
f1_keywords: 
 - "shlobj_core/IActiveDesktop.SetWallpaper"
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
 - IActiveDesktop.SetWallpaper
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>
 

 

