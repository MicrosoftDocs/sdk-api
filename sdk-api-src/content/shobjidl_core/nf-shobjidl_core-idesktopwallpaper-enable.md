---
UID: NF:shobjidl_core.IDesktopWallpaper.Enable
title: IDesktopWallpaper::Enable (shobjidl_core.h)
author: windows-sdk-content
description: Enables or disables the desktop background.
old-location: shell\IDesktopWallpaper_Enable.htm
tech.root: shell
ms.assetid: 8BC04B93-4BF4-4713-8EF8-C4BCF1C8090E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Enable, Enable method [Windows Shell], Enable method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],Enable method, IDesktopWallpaper.Enable, IDesktopWallpaper::Enable, shell.IDesktopWallpaper_Enable, shobjidl_core/IDesktopWallpaper::Enable
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
 - IDesktopWallpaper.Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDesktopWallpaper::Enable


## -description


Enables or disables the desktop background.


## -parameters




### -param enable [in]

<b>TRUE</b> to enable the desktop background, <b>FALSE</b> to disable it.


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
The desktop wallpaper is already in the state you're asking for through this call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The desktop wallpaper that would be used when the background is enabled is missing from its expected location. Call <a href="https://msdn.microsoft.com/5E0731DC-8B70-40dc-B90A-97B1E3E4D55D">SetWallpaper</a> to specify a new wallpaper.

</td>
</tr>
</table>
 




## -remarks



This method would normally be called to disable the desktop background for performance reasons.

When the desktop background is disabled, a solid color is shown in its place. To get or set the specific color, use the <a href="https://msdn.microsoft.com/92666512-BE10-4ee7-B670-18F0C714A4C9">GetBackgroundColor</a> and <a href="https://msdn.microsoft.com/9CA14C0B-4727-4702-9EB0-4D24003EB456">SetBackgroundColor</a> methods.

<div class="alert"><b>Note</b>  A call to the <a href="https://msdn.microsoft.com/5E0731DC-8B70-40dc-B90A-97B1E3E4D55D">IDesktopWallpaper_SetWallpaper</a> or <a href="https://msdn.microsoft.com/0E4743A0-75AB-456a-BAAE-8EC4C0D14E6C">IDesktopWallpaper_SetSlideshow</a> methods will enable the desktop background even if it is currently disabled through this method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>
 

 

