---
UID: NF:shobjidl_core.IDesktopWallpaper.AdvanceSlideshow
title: IDesktopWallpaper::AdvanceSlideshow
author: windows-sdk-content
description: Switches the wallpaper on a specified monitor to the next image in the slideshow.
old-location: shell\IDesktopWallpaper_AdvanceSlideshow.htm
tech.root: shell
ms.assetid: A68F6EFA-DD74-453f-A7D3-7CEC2E760FD1
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: AdvanceSlideshow, AdvanceSlideshow method [Windows Shell], AdvanceSlideshow method [Windows Shell],IDesktopWallpaper interface, DSD_BACKWARD, DSD_FORWARD, IDesktopWallpaper interface [Windows Shell],AdvanceSlideshow method, IDesktopWallpaper.AdvanceSlideshow, IDesktopWallpaper::AdvanceSlideshow, shell.IDesktopWallpaper_AdvanceSlideshow, shobjidl_core/IDesktopWallpaper::AdvanceSlideshow
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
 - IDesktopWallpaper.AdvanceSlideshow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDesktopWallpaper::AdvanceSlideshow


## -description


Switches the wallpaper on a specified monitor to the next image in the slideshow.


## -parameters




### -param monitorID [in]

The ID of the monitor on which to change the wallpaper image. This ID can be obtained through the <a href="https://msdn.microsoft.com/CE0C6B07-F9D1-4221-9D9D-8D17CF6780E6">GetMonitorDevicePathAt</a> method. If this parameter is set to <b>NULL</b>, the monitor scheduled to change next is used.


### -param direction [in]

The direction that the slideshow should advance. One of the following DESKTOP_SLIDESHOW_DIRECTION values:



#### DSD_FORWARD (0)

Advance the slideshow forward.



#### DSD_BACKWARD (1)

Advance the slideshow backward.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>
 

 

