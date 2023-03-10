---
UID: NF:shobjidl_core.IDesktopWallpaper.SetPosition
title: IDesktopWallpaper::SetPosition (shobjidl_core.h)
description: Sets the display option for the desktop wallpaper image, determining whether the image should be centered, tiled, or stretched.
helpviewer_keywords: ["IDesktopWallpaper interface [Windows Shell]","SetPosition method","IDesktopWallpaper.SetPosition","IDesktopWallpaper::SetPosition","SetPosition","SetPosition method [Windows Shell]","SetPosition method [Windows Shell]","IDesktopWallpaper interface","shell.IDesktopWallpaper_SetPosition","shobjidl_core/IDesktopWallpaper::SetPosition"]
old-location: shell\IDesktopWallpaper_SetPosition.htm
tech.root: shell
ms.assetid: A4993DB8-9132-43c1-B900-02BA5384B7A8
ms.date: 12/05/2018
ms.keywords: IDesktopWallpaper interface [Windows Shell],SetPosition method, IDesktopWallpaper.SetPosition, IDesktopWallpaper::SetPosition, SetPosition, SetPosition method [Windows Shell], SetPosition method [Windows Shell],IDesktopWallpaper interface, shell.IDesktopWallpaper_SetPosition, shobjidl_core/IDesktopWallpaper::SetPosition
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDesktopWallpaper::SetPosition
 - shobjidl_core/IDesktopWallpaper::SetPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDesktopWallpaper.SetPosition
---

# IDesktopWallpaper::SetPosition


## -description

Sets the display option for the desktop wallpaper image, determining whether the image should be centered, tiled, or stretched.

## -parameters

### -param position [in]

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position">DESKTOP_WALLPAPER_POSITION</a> enumeration values that specify how the image will be displayed on the system's monitors.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The desktop wallpaper is already displayed as asked for in <i>position</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getposition">IDesktopWallpaper::GetPosition</a>