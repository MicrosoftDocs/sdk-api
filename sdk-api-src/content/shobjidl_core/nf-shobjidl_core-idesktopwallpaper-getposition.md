---
UID: NF:shobjidl_core.IDesktopWallpaper.GetPosition
title: IDesktopWallpaper::GetPosition
author: windows-sdk-content
description: Retrieves the current display value for the desktop background image.
old-location: shell\IDesktopWallpaper_GetPosition.htm
tech.root: shell
ms.assetid: 28D057DD-63CF-4078-9E0C-7DB61E1683EF
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetPosition, GetPosition method [Windows Shell], GetPosition method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetPosition method, IDesktopWallpaper.GetPosition, IDesktopWallpaper::GetPosition, shell.IDesktopWallpaper_GetPosition, shobjidl_core/IDesktopWallpaper::GetPosition
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
 - IDesktopWallpaper.GetPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDesktopWallpaper::GetPosition


## -description


Retrieves the current display value for the desktop background image.


## -parameters




### -param position [out]

A pointer to a value that, when this method returns successfully, receives one of the <a href="https://msdn.microsoft.com/5524E7DA-087C-475a-BB22-5E62C1A5CC4D">DESKTOP_WALLPAPER_POSITION</a> enumeration values that specify how the image is being displayed on the system's monitors.


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




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/A4993DB8-9132-43c1-B900-02BA5384B7A8">IDesktopWallpaper::SetPosition</a>
 

 

