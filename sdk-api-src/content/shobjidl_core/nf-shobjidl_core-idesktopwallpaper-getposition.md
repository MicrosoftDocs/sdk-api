---
UID: NF:shobjidl_core.IDesktopWallpaper.GetPosition
title: IDesktopWallpaper::GetPosition (shobjidl_core.h)
description: Retrieves the current display value for the desktop background image.
helpviewer_keywords: ["GetPosition","GetPosition method [Windows Shell]","GetPosition method [Windows Shell]","IDesktopWallpaper interface","IDesktopWallpaper interface [Windows Shell]","GetPosition method","IDesktopWallpaper.GetPosition","IDesktopWallpaper::GetPosition","shell.IDesktopWallpaper_GetPosition","shobjidl_core/IDesktopWallpaper::GetPosition"]
old-location: shell\IDesktopWallpaper_GetPosition.htm
tech.root: shell
ms.assetid: 28D057DD-63CF-4078-9E0C-7DB61E1683EF
ms.date: 12/05/2018
ms.keywords: GetPosition, GetPosition method [Windows Shell], GetPosition method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetPosition method, IDesktopWallpaper.GetPosition, IDesktopWallpaper::GetPosition, shell.IDesktopWallpaper_GetPosition, shobjidl_core/IDesktopWallpaper::GetPosition
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
 - IDesktopWallpaper::GetPosition
 - shobjidl_core/IDesktopWallpaper::GetPosition
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
 - IDesktopWallpaper.GetPosition
---

# IDesktopWallpaper::GetPosition


## -description

Retrieves the current display value for the desktop background image.

## -parameters

### -param position [out]

A pointer to a value that, when this method returns successfully, receives one of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position">DESKTOP_WALLPAPER_POSITION</a> enumeration values that specify how the image is being displayed on the system's monitors.

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

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper">IDesktopWallpaper</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setposition">IDesktopWallpaper::SetPosition</a>