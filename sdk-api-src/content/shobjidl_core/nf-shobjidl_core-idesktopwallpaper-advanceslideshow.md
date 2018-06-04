---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

