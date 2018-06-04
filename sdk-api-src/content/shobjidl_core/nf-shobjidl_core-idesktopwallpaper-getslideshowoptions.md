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
 

 

