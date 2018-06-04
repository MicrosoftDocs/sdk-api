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

# IMFMediaEngine::OnVideoStreamTick


## -description


Queries the Media Engine to find out whether a new video frame is ready.


## -parameters




### -param pPts [out]

If a new frame is ready, receives the presentation time of the frame.


## -returns



This method can return one of these values.

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
The method succeeded, but the Media Engine does not have a new frame.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
A new video frame is ready for display.

</td>
</tr>
</table>
 




## -remarks



In frame-server mode, the application should call this method whenever a vertical blank occurs in the display device. If the method returns <b>S_OK</b>, call <a href="https://msdn.microsoft.com/07DB29E2-9F09-46CB-B138-197D95EC37F0">IMFMediaEngine::TransferVideoFrame</a> to blit the frame to the render target. If the method returns <b>S_FALSE</b>, wait for the next vertical blank and call the method again.

Do not call this method in rendering mode or audio-only mode. 




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

