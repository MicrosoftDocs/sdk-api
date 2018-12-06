---
UID: NN:shobjidl_core.IDesktopWallpaper
title: IDesktopWallpaper
author: windows-sdk-content
description: "."
old-location: shell\IDesktopWallpaper.htm
tech.root: shell
ms.assetid: A83903B5-314B-4a8b-8D37-F8A8995DE0CB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDesktopWallpaper, IDesktopWallpaper interface [Windows Shell], IDesktopWallpaper interface [Windows Shell],described, shell.IDesktopWallpaper, shobjidl_core/IDesktopWallpaper
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IDesktopWallpaper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDesktopWallpaper interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDesktopWallpaper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDesktopWallpaper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDesktopWallpaper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A68F6EFA-DD74-453f-A7D3-7CEC2E760FD1">AdvanceSlideshow</a>
</td>
<td align="left" width="63%">
Switches the wallpaper on a specified monitor to the next image in the slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8BC04B93-4BF4-4713-8EF8-C4BCF1C8090E">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables the desktop background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92666512-BE10-4ee7-B670-18F0C714A4C9">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CE0C6B07-F9D1-4221-9D9D-8D17CF6780E6">GetMonitorDevicePathAt</a>
</td>
<td align="left" width="63%">
Retrieves the unique ID of one of the system's monitors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E7490E24-7BCE-4fbb-8512-998EAE045CE7">GetMonitorDevicePathCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of monitors that are associated with the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98A3F193-DBCF-42ec-9283-53F0F46BB1C4">GetMonitorRECT</a>
</td>
<td align="left" width="63%">
Retrieves the display rectangle of the specified monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28D057DD-63CF-4078-9E0C-7DB61E1683EF">GetPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current display value for the desktop background image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A5660D7F-C42A-4587-B319-B47441CD37AB">GetSlideshow</a>
</td>
<td align="left" width="63%">
Gets the images that are being displayed in the desktop wallpaper slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2EB99E61-F5B4-4f07-8A87-793BE59D309B">GetSlideshowOptions</a>
</td>
<td align="left" width="63%">
Gets the current desktop wallpaper slideshow settings for shuffle and timing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19F2776E-0B5F-45c9-962A-08BFC0273066">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the current status of the slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A5AC5EB3-2091-4547-8B6A-C60C4E90DFBC">GetWallpaper</a>
</td>
<td align="left" width="63%">
Gets the current desktop wallpaper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9CA14C0B-4727-4702-9EB0-4D24003EB456">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4993DB8-9132-43c1-B900-02BA5384B7A8">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the display option for the desktop wallpaper image, determining whether the image should be centered, tiled, or stretched.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0E4743A0-75AB-456a-BAAE-8EC4C0D14E6C">SetSlideshow</a>
</td>
<td align="left" width="63%">
Specifies the images to use for the desktop wallpaper slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B3106354-C321-4770-834F-D2EF790AE114">SetSlideshowOptions</a>
</td>
<td align="left" width="63%">
Sets the desktop wallpaper slideshow settings for shuffle and timing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5E0731DC-8B70-40dc-B90A-97B1E3E4D55D">SetWallpaper</a>
</td>
<td align="left" width="63%">
Sets the desktop wallpaper.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

