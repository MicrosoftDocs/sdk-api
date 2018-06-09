---
UID: NF:shobjidl_core.IDesktopWallpaper.GetStatus
title: IDesktopWallpaper::GetStatus
author: windows-sdk-content
description: Gets the current status of the slideshow.
old-location: shell\IDesktopWallpaper_GetStatus.htm
old-project: shell
ms.assetid: 19F2776E-0B5F-45c9-962A-08BFC0273066
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: DSS_DISABLED_BY_REMOTE_SESSION, DSS_ENABLED, DSS_SLIDESHOW, GetStatus, GetStatus method [Windows Shell], GetStatus method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetStatus method, IDesktopWallpaper.GetStatus, IDesktopWallpaper::GetStatus, shell.IDesktopWallpaper_GetStatus, shobjidl_core/IDesktopWallpaper::GetStatus
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
 - IDesktopWallpaper.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDesktopWallpaper::GetStatus


## -description


Gets the current status of the slideshow.


## -parameters




### -param state [out]

A pointer to a DESKTOP_SLIDESHOW_STATE value that, when this method returns successfully, receives one or more of the following flags.



#### DSS_ENABLED (0x01)

Slideshows are enabled.



#### DSS_SLIDESHOW (0x02)

A slideshow is currently configured.



#### DSS_DISABLED_BY_REMOTE_SESSION (0x04)

A remote session has temporarily disabled the slideshow.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>
 

 

