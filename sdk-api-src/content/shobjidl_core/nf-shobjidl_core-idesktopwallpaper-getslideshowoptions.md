---
UID: NF:shobjidl_core.IDesktopWallpaper.GetSlideshowOptions
title: IDesktopWallpaper::GetSlideshowOptions
author: windows-sdk-content
description: Gets the current desktop wallpaper slideshow settings for shuffle and timing.
old-location: shell\IDesktopWallpaper_GetSlideshowOptions.htm
old-project: shell
ms.assetid: 2EB99E61-F5B4-4f07-8A87-793BE59D309B
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DSO_SHUFFLEIMAGES, GetSlideshowOptions, GetSlideshowOptions method [Windows Shell], GetSlideshowOptions method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetSlideshowOptions method, IDesktopWallpaper.GetSlideshowOptions, IDesktopWallpaper::GetSlideshowOptions, shell.IDesktopWallpaper_GetSlideshowOptions, shobjidl_core/IDesktopWallpaper::GetSlideshowOptions
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
 - IDesktopWallpaper.GetSlideshowOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDesktopWallpaper::GetSlideshowOptions


## -description


Gets the current desktop wallpaper slideshow settings for shuffle and timing.


## -parameters




### -param options [out]

Type: <b>DESKTOP_SLIDESHOW_OPTIONS*</b>

A pointer to a value that, when this method returns successfully, receives either 0 to indicate that shuffle is disabled or the following value.



#### DSO_SHUFFLEIMAGES (0x01)

Shuffle is enabled; the images are shown in a random order.


### -param slideshowTick [out]

Type: <b>UINT*</b>

A pointer to a value that, when this method returns successfully, receives the interval between image transitions, in milliseconds.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code, including the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided in one of the parameters.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/B3106354-C321-4770-834F-D2EF790AE114">IDesktopWallpaper::SetSlideshowOptions</a>
 

 

