---
UID: NF:shobjidl_core.IDesktopWallpaper.SetBackgroundColor
title: IDesktopWallpaper::SetBackgroundColor
author: windows-sdk-content
description: Sets the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.
old-location: shell\IDesktopWallpaper_SetBackgroundColor.htm
old-project: shell
ms.assetid: 9CA14C0B-4727-4702-9EB0-4D24003EB456
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDesktopWallpaper interface [Windows Shell],SetBackgroundColor method, IDesktopWallpaper.SetBackgroundColor, IDesktopWallpaper::SetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [Windows Shell], SetBackgroundColor method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetBackgroundColor, shobjidl_core/IDesktopWallpaper::SetBackgroundColor
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
 - IDesktopWallpaper.SetBackgroundColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDesktopWallpaper::SetBackgroundColor


## -description


Sets the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.


## -parameters




### -param color [in]

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that specifies the background RGB color value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/92666512-BE10-4ee7-B670-18F0C714A4C9">IDesktopWallpaper::GetBackgroundColor</a>
 

 

