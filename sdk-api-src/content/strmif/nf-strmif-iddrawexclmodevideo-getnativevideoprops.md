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

# IDDrawExclModeVideo::GetNativeVideoProps


## -description



The <code>GetNativeVideoProps</code> method retrieves the current video size and picture aspect ratio of the Overlay Mixer's primary stream.




## -parameters




### -param pdwVideoWidth [out]

Address of variable that receives the width of the video.


### -param pdwVideoHeight [out]

Address of variable that receives the height of the video.


### -param pdwPictAspectRatioX [out]

Address of variable that receives the x-axis aspect ratio.


### -param pdwPictAspectRatioY [out]

Address of variable that receives the y-axis aspect ratio.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
</table>
 




## -remarks



The filter graph should look for the <a href="https://msdn.microsoft.com/276f37b3-f981-4a01-bb37-1ee77248668f">EC_VIDEO_SIZE_CHANGED</a> event, and on its receipt call this method to adjust the aspect ratio and position.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo Interface</a>
 

 

