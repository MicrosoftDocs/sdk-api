---
UID: NN:comsvcs.IPlaybackControl
title: IPlaybackControl (comsvcs.h)
description: Enables participation in the abnormal handling of server-side playback errors and client-side failures of the Message Queuing delivery mechanism.helpviewer_keywords: ["IPlaybackControl","IPlaybackControl interface [COM+]","IPlaybackControl interface [COM+]","described","_cos_IPlaybackControl","comsvcs/IPlaybackControl","cos.iplaybackcontrol"]
old-location: cos\iplaybackcontrol.htm
tech.root: cossdk
ms.assetid: 3a528e92-37ac-4108-b52a-557a90da4a47
ms.date: 12/05/2018
ms.keywords: IPlaybackControl, IPlaybackControl interface [COM+], IPlaybackControl interface [COM+],described, _cos_IPlaybackControl, comsvcs/IPlaybackControl, cos.iplaybackcontrol
f1_keywords:
- comsvcs/IPlaybackControl
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPlaybackControl interface


## -description


Enables participation in the abnormal handling of server-side playback errors and client-side failures of the Message Queuing delivery mechanism. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPlaybackControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPlaybackControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iplaybackcontrol-finalclientretry">FinalClientRetry</a>
</td>
<td align="left" width="63%">
Informs the client-side exception handling component that all Message Queuing attempts to deliver the message to the server were rejected. The message ended up on the client-side Xact dead letter queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iplaybackcontrol-finalserverretry">FinalServerRetry</a>
</td>
<td align="left" width="63%">
Informs the server-side Exception_CLSID implementation that all attempts to play back the deferred activation have failed. The message is about to be moved to the final resting queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--queued-components">COM+ Queued Components</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-imessagemover">IMessageMover</a>
 

 

