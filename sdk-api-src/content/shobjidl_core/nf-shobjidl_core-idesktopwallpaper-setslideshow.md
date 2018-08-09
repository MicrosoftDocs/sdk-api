---
UID: NF:shobjidl_core.IDesktopWallpaper.SetSlideshow
title: IDesktopWallpaper::SetSlideshow
author: windows-sdk-content
description: Specifies the images to use for the desktop wallpaper slideshow.
old-location: shell\IDesktopWallpaper_SetSlideshow.htm
old-project: shell
ms.assetid: 0E4743A0-75AB-456a-BAAE-8EC4C0D14E6C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDesktopWallpaper interface [Windows Shell],SetSlideshow method, IDesktopWallpaper.SetSlideshow, IDesktopWallpaper::SetSlideshow, SetSlideshow, SetSlideshow method [Windows Shell], SetSlideshow method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetSlideshow, shobjidl_core/IDesktopWallpaper::SetSlideshow
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
 - IDesktopWallpaper.SetSlideshow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDesktopWallpaper::SetSlideshow


## -description


Specifies the images to use for the desktop wallpaper slideshow.


## -parameters




### -param items [in]

A pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a> that contains the slideshow images. This array can contain individual items stored in the same container (files stored in a folder), or it can contain a single item which is the container itself (a folder that contains images). Any other configuration of the array will cause this method to fail.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/A5660D7F-C42A-4587-B319-B47441CD37AB">IDesktopWallpaper::GetSlideshow</a>
 

 

