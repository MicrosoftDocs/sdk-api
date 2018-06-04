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

# IMFVideoPresenter interface


## -description


Represents a video presenter. A <i>video presenter</i> is an object that receives video frames, typically from a video mixer, and presents them in some way, typically by rendering them to the display. The enhanced video renderer (EVR) provides a default video presenter, and applications can implement custom presenters.

The video presenter receives video frames as soon as they are available from upstream. The video presenter is responsible for presenting frames at the correct time and for synchronizing with the presentation clock.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoPresenter</b> interface inherits from <a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>. <b>IMFVideoPresenter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoPresenter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b8f0e56-35de-4b4f-9897-32a7e14171c8">GetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the presenter's media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7113cb3-2ea9-4d4f-b6c7-ef4e1025cc6d">ProcessMessage</a>
</td>
<td align="left" width="63%">
Sends a message to the video presenter.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

