---
UID: NF:shobjidl_core.IDesktopWallpaper.SetWallpaper
title: IDesktopWallpaper::SetWallpaper
author: windows-sdk-content
description: Sets the desktop wallpaper.
old-location: shell\IDesktopWallpaper_SetWallpaper.htm
old-project: shell
ms.assetid: 5E0731DC-8B70-40dc-B90A-97B1E3E4D55D
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IDesktopWallpaper interface [Windows Shell],SetWallpaper method, IDesktopWallpaper.SetWallpaper, IDesktopWallpaper::SetWallpaper, SetWallpaper, SetWallpaper method [Windows Shell], SetWallpaper method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetWallpaper, shobjidl_core/IDesktopWallpaper::SetWallpaper
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDesktopWallpaper.SetWallpaper
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDesktopWallpaper::SetWallpaper


## -description


Sets the desktop wallpaper.


## -parameters




### -param monitorID [in]

The ID of the monitor. This value can be obtained through <a href="https://msdn.microsoft.com/CE0C6B07-F9D1-4221-9D9D-8D17CF6780E6">GetMonitorDevicePathAt</a>. Set this value to NULL to set the wallpaper image on all monitors.


### -param wallpaper [in]

The full path of the wallpaper image file.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/A5AC5EB3-2091-4547-8B6A-C60C4E90DFBC">IDesktopWallpaper::GetWallpaper</a>
 

 

