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

# DESKTOP_WALLPAPER_POSITION enumeration


## -description


Specifies how the desktop wallpaper should be displayed.


## -enum-fields




### -field DWPOS_CENTER

Center the image; do not stretch. This is equivalent to the <a href="https://msdn.microsoft.com/6d1a2f69-0730-4805-8b50-071332ff7070">WPSTYLE_CENTER</a> style in <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>.


### -field DWPOS_TILE

Tile the image across all monitors. This is equivalent to the <a href="https://msdn.microsoft.com/6d1a2f69-0730-4805-8b50-071332ff7070">WPSTYLE_TILE</a> style in <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>.


### -field DWPOS_STRETCH

Stretch the image to exactly fit on the monitor. This is equivalent to the <a href="https://msdn.microsoft.com/6d1a2f69-0730-4805-8b50-071332ff7070">WPSTYLE_STRETCH</a> style in <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>.


### -field DWPOS_FIT

Stretch the image to exactly the height or width of the monitor without changing its aspect ratio or cropping the image. This can result in <a href="https://msdn.microsoft.com/92666512-BE10-4ee7-B670-18F0C714A4C9">colored letterbox bars</a> on either side or on above and below of the image. This is equivalent to the <a href="https://msdn.microsoft.com/6d1a2f69-0730-4805-8b50-071332ff7070">WPSTYLE_KEEPASPECT</a> style in <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>.


### -field DWPOS_FILL

Stretch the image to fill the screen, cropping the image as necessary to avoid letterbox bars. This is equivalent to the <a href="https://msdn.microsoft.com/6d1a2f69-0730-4805-8b50-071332ff7070">WPSTYLE_CROPTOFIT</a> style in <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>.


### -field DWPOS_SPAN

Spans a single image across all monitors attached to the system. This flag has no <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a> equivalent.


## -see-also




<a href="https://msdn.microsoft.com/28D057DD-63CF-4078-9E0C-7DB61E1683EF">IDesktopWallpaper::GetPosition</a>



<a href="https://msdn.microsoft.com/A4993DB8-9132-43c1-B900-02BA5384B7A8">IDesktopWallpaper::SetPosition</a>
 

 

