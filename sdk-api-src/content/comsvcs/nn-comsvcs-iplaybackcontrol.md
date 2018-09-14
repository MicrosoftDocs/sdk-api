---
UID: NN:comsvcs.IPlaybackControl
title: IPlaybackControl
author: windows-sdk-content
description: Enables participation in the abnormal handling of server-side playback errors and client-side failures of the Message Queuing delivery mechanism.
old-location: cos\iplaybackcontrol.htm
tech.root: cossdk
ms.assetid: 3a528e92-37ac-4108-b52a-557a90da4a47
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IPlaybackControl, IPlaybackControl interface [COM+], IPlaybackControl interface [COM+],described, _cos_IPlaybackControl, comsvcs/IPlaybackControl, cos.iplaybackcontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ComSvcs.h
api_name:
 - IPlaybackControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPlaybackControl interface


## -description


Enables participation in the abnormal handling of server-side playback errors and client-side failures of the Message Queuing delivery mechanism. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPlaybackControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPlaybackControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPlaybackControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fa51832-0e68-4e76-bbdb-ce54f76fbae6">FinalClientRetry</a>
</td>
<td align="left" width="63%">
Informs the client-side exception handling component that all Message Queuing attempts to deliver the message to the server were rejected. The message ended up on the client-side Xact dead letter queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03f0bd46-004d-4ed6-b00b-de765d339ba0">FinalServerRetry</a>
</td>
<td align="left" width="63%">
Informs the server-side Exception_CLSID implementation that all attempts to play back the deferred activation have failed. The message is about to be moved to the final resting queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/810305ad-c7fb-4627-8ca7-de37c5bef2f5">COM+ Queued Components</a>



<a href="https://msdn.microsoft.com/aa7c57a2-0dee-4f18-bce4-4fcc47d4d7a7">IMessageMover</a>
 

 

