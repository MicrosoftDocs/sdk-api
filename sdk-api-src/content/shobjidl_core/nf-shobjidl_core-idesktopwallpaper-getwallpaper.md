---
UID: NF:shobjidl_core.IDesktopWallpaper.GetWallpaper
title: IDesktopWallpaper::GetWallpaper
author: windows-sdk-content
description: Gets the current desktop wallpaper.
old-location: shell\IDesktopWallpaper_GetWallpaper.htm
tech.root: shell
ms.assetid: A5AC5EB3-2091-4547-8B6A-C60C4E90DFBC
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetWallpaper, GetWallpaper method [Windows Shell], GetWallpaper method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetWallpaper method, IDesktopWallpaper.GetWallpaper, IDesktopWallpaper::GetWallpaper, shell.IDesktopWallpaper_GetWallpaper, shobjidl_core/IDesktopWallpaper::GetWallpaper
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDesktopWallpaper.GetWallpaper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDesktopWallpaper::GetWallpaper


## -description


Gets the current desktop wallpaper.


## -parameters




### -param monitorID [in]

The ID of the monitor. This value can be obtained through <a href="https://msdn.microsoft.com/CE0C6B07-F9D1-4221-9D9D-8D17CF6780E6">GetMonitorDevicePathAt</a>.

This value can be set to <b>NULL</b>. In that case, if a single wallpaper image is displayed on all of the system's monitors, the method returns successfully. If this value is set to <b>NULL</b> and different monitors are displaying different wallpapers or a slideshow is running, the method returns S_FALSE and an empty string in the <i>wallpaper</i> parameter.


### -param wallpaper [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the path to the wallpaper image file. Note that this image could be currently displayed on all of the system's monitors, not just the monitor specified in the <i>monitorID</i> parameter.

This string will be empty if no wallpaper image is being displayed or if a monitor is displaying a solid color. The string will also be empty if the method fails.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/5E0731DC-8B70-40dc-B90A-97B1E3E4D55D">IDesktopWallpaper::SetWallpaper</a>
 

 

