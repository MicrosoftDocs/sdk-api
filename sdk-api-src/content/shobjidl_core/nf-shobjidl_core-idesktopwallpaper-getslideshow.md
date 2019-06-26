---
UID: NF:shobjidl_core.IDesktopWallpaper.GetSlideshow
title: IDesktopWallpaper::GetSlideshow (shobjidl_core.h)
author: windows-sdk-content
description: Gets the images that are being displayed in the desktop wallpaper slideshow.
old-location: shell\IDesktopWallpaper_GetSlideshow.htm
tech.root: shell
ms.assetid: A5660D7F-C42A-4587-B319-B47441CD37AB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSlideshow, GetSlideshow method [Windows Shell], GetSlideshow method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetSlideshow method, IDesktopWallpaper.GetSlideshow, IDesktopWallpaper::GetSlideshow, shell.IDesktopWallpaper_GetSlideshow, shobjidl_core/IDesktopWallpaper::GetSlideshow
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IDesktopWallpaper.GetSlideshow"
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
 - IDesktopWallpaper.GetSlideshow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDesktopWallpaper::GetSlideshow


## -description


Gets the images that are being displayed in the desktop wallpaper slideshow.


## -parameters




### -param items [out]

The address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a> object that, when this method returns successfully, receives the items that make up the slideshow. This array can contain individual items stored in the same container, or it can contain a single item which is the container itself.


## -returns



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
A <b>NULL</b> pointer was provided in <i>position</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setslideshow">IDesktopWallpaper::SetSlideshow</a>
 

 

