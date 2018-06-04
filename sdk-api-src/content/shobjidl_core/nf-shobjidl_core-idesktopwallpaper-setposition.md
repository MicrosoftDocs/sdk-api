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

# IDesktopWallpaper::SetPosition


## -description


Sets the display option for the desktop wallpaper image, determining whether the image should be centered, tiled, or stretched.


## -parameters




### -param position [in]

One of the <a href="https://msdn.microsoft.com/5524E7DA-087C-475a-BB22-5E62C1A5CC4D">DESKTOP_WALLPAPER_POSITION</a> enumeration values that specify how the image will be displayed on the system's monitors.


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




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/28D057DD-63CF-4078-9E0C-7DB61E1683EF">IDesktopWallpaper::GetPosition</a>
 

 

