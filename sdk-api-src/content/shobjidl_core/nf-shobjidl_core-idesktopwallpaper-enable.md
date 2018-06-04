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
 

 

