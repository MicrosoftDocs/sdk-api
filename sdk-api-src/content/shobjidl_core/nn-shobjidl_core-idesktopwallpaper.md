---
UID: NN:shobjidl_core.IDesktopWallpaper
title: IDesktopWallpaper (shobjidl_core.h)
description: .helpviewer_keywords: ["IDesktopWallpaper","IDesktopWallpaper interface [Windows Shell]","IDesktopWallpaper interface [Windows Shell]","described","shell.IDesktopWallpaper","shobjidl_core/IDesktopWallpaper"]
old-location: shell\IDesktopWallpaper.htm
tech.root: shell
ms.assetid: A83903B5-314B-4a8b-8D37-F8A8995DE0CB
ms.date: 12/05/2018
ms.keywords: IDesktopWallpaper, IDesktopWallpaper interface [Windows Shell], IDesktopWallpaper interface [Windows Shell],described, shell.IDesktopWallpaper, shobjidl_core/IDesktopWallpaper
f1_keywords:
- shobjidl_core/IDesktopWallpaper
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDesktopWallpaper interface


## -description

Provides methods for managing the desktop wallpaper.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDesktopWallpaper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDesktopWallpaper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-advanceslideshow">AdvanceSlideshow</a>
</td>
<td align="left" width="63%">
Switches the wallpaper on a specified monitor to the next image in the slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-enable">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables the desktop background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getbackgroundcolor">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathat">GetMonitorDevicePathAt</a>
</td>
<td align="left" width="63%">
Retrieves the unique ID of one of the system's monitors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitordevicepathcount">GetMonitorDevicePathCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of monitors that are associated with the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getmonitorrect">GetMonitorRECT</a>
</td>
<td align="left" width="63%">
Retrieves the display rectangle of the specified monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getposition">GetPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current display value for the desktop background image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getslideshow">GetSlideshow</a>
</td>
<td align="left" width="63%">
Gets the images that are being displayed in the desktop wallpaper slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getslideshowoptions">GetSlideshowOptions</a>
</td>
<td align="left" width="63%">
Gets the current desktop wallpaper slideshow settings for shuffle and timing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the current status of the slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getwallpaper">GetWallpaper</a>
</td>
<td align="left" width="63%">
Gets the current desktop wallpaper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setbackgroundcolor">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the color that is visible on the desktop when no image is displayed or when the desktop background has been disabled. This color is also used as a border when the desktop wallpaper does not fill the entire screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setposition">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the display option for the desktop wallpaper image, determining whether the image should be centered, tiled, or stretched.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setslideshow">SetSlideshow</a>
</td>
<td align="left" width="63%">
Specifies the images to use for the desktop wallpaper slideshow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setslideshowoptions">SetSlideshowOptions</a>
</td>
<td align="left" width="63%">
Sets the desktop wallpaper slideshow settings for shuffle and timing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setwallpaper">SetWallpaper</a>
</td>
<td align="left" width="63%">
Sets the desktop wallpaper.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

