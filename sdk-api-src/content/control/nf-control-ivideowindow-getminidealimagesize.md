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

# IVideoWindow::GetMinIdealImageSize


## -description



The <code>GetMinIdealImageSize</code> method retrieves the minimum ideal size for the video image.




## -parameters




### -param pWidth [out]


            Receives the minimum ideal width, in pixels.
          


### -param pHeight [out]

Receives the minimum ideal height, in pixels.
          


## -returns



Possible return values include the following:

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
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not retrieve a minimum image size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter is stopped.

</td>
</tr>
</table>
 




## -remarks



The maximum ideal size may differ from the native video size, because the video hardware might have specific stretching requirements.

This method returns S_FALSE under various circumstances:

<ul>
<li>The filter is using an <a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay</a> transport.</li>
<li>
            UseWhenFullScreen mode is on. (See <a href="https://msdn.microsoft.com/e50f7f06-6534-4373-a2b8-fa315158729d">IDirectDrawVideo::UseWhenFullScreen</a>.)</li>
<li>Video playback is using a stretchable offscreen surface. (The <b>dwCaps</b> member of the DDCAPS structure includes the DDCAPS_BLTSTRETCH flag. See <a href="https://msdn.microsoft.com/d63437e3-4e8a-49de-b555-db29d235569d">IDirectDrawVideo::GetCaps</a>.)</li>
<li>The video surface has no minimum overlay stretch. (The <b>dwMinOverlayStretch</b> member of the DDCAPS structure is zero. See <a href="https://msdn.microsoft.com/d63437e3-4e8a-49de-b555-db29d235569d">IDirectDrawVideo::GetCaps</a>.)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/ee9f6803-c8b8-48e0-9be0-3d61a453014e">IVideoWindow::GetMaxIdealImageSize</a>
 

 

