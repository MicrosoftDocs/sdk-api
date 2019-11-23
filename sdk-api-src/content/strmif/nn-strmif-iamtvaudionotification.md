---
UID: NN:strmif.IAMTVAudioNotification
title: IAMTVAudioNotification (strmif.h)

description: Note  This callback interface has been deprecated, because the TV Audio filter does not implement the callback mechanism. .
old-location: dshow\iamtvaudionotification.htm
tech.root: DirectShow
ms.assetid: 4f84586f-7384-4dd7-99ce-325fb609daae

ms.date: 12/05/2018
ms.keywords: IAMTVAudioNotification, IAMTVAudioNotification interface [DirectShow], IAMTVAudioNotification interface [DirectShow],described, IAMTVAudioNotificationInterface, dshow.iamtvaudionotification, strmif/IAMTVAudioNotification
ms.topic: interface
f1_keywords: 
 - "strmif/IAMTVAudioNotification"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMTVAudioNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTVAudioNotification interface


## -description



<div class="alert"><b>Note</b>  This callback interface has been deprecated, because the TV Audio filter does not implement the callback mechanism.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTVAudioNotification</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTVAudioNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTVAudioNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvaudionotification-onevent">OnEvent</a>
</td>
<td align="left" width="63%">
Handles events from a TV tuner card controlled by the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

