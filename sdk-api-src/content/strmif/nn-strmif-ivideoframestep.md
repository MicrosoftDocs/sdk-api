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

# IVideoFrameStep interface


## -description



The <code>IVideoFrameStep</code> interface steps through a video stream. This interface enables Microsoft® DirectShow® applications, including DVD players, to step through a video stream as slowly as one frame at a time. Obtain the interface through the filter graph manager, which controls the frame stepping process in conjunction with the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer Filter</a> or the Video Renderer Filter. Backward frame stepping is not supported.

<div class="alert"><b>Note</b>  
           For frame stepping to work with a hardware decoder, the decoder must support the <a href="https://msdn.microsoft.com/01abe1fe-fc2f-44cb-9546-45a8d682a179">Frame Stepping Property Set</a>.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVideoFrameStep</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVideoFrameStep</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVideoFrameStep</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1310d4d8-a1a3-493c-baee-f7c0ec5790e1">CancelStep</a>
</td>
<td align="left" width="63%">
Cancels the previous step operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2e3f665-28be-4a6d-b29a-4f0485d9a672">CanStep</a>
</td>
<td align="left" width="63%">
Determines the stepping capabilities of the specified filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1366b8b4-ea7a-4528-8a5a-03a3de265d89">Step</a>
</td>
<td align="left" width="63%">
Causes the filter graph to step forward by the specified number of frames.

</td>
</tr>
</table> 

