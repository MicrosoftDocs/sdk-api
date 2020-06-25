---
UID: NN:mfobjects.IMFMediaEventGenerator
title: IMFMediaEventGenerator (mfobjects.h)
description: Retrieves events from any Media Foundation object that generates events.
helpviewer_keywords: ["IMFMediaEventGenerator","IMFMediaEventGenerator interface [Media Foundation]","IMFMediaEventGenerator interface [Media Foundation]","described","a37d0840-c896-43a0-b3d1-c2a6aaff1b25","mf.imfmediaeventgenerator","mfobjects/IMFMediaEventGenerator"]
old-location: mf\imfmediaeventgenerator.htm
tech.root: medfound
ms.assetid: a37d0840-c896-43a0-b3d1-c2a6aaff1b25
ms.date: 12/05/2018
ms.keywords: IMFMediaEventGenerator, IMFMediaEventGenerator interface [Media Foundation], IMFMediaEventGenerator interface [Media Foundation],described, a37d0840-c896-43a0-b3d1-c2a6aaff1b25, mf.imfmediaeventgenerator, mfobjects/IMFMediaEventGenerator
f1_keywords:
- mfobjects/IMFMediaEventGenerator
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFMediaEventGenerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEventGenerator interface


## -description


Retrieves events from any Media Foundation object that generates events.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEventGenerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEventGenerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEventGenerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent">BeginGetEvent</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">EndGetEvent</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent">GetEvent</a>
</td>
<td align="left" width="63%">
Retrieves the next event in the queue. This method is synchronous.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent">QueueEvent</a>
</td>
<td align="left" width="63%">
Puts a new event in the object's queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/remotebegingetevent">RemoteBeginGetEvent</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent">BeginGetEvent</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/remoteendgetevent">RemoteEndGetEvent</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">EndGetEvent</a>. (Not used by applications.)

</td>
</tr>
</table> 


## -remarks



An object that supports this interface maintains a queue of events. The client of the object can retrieve the events either synchronously or asynchronously. The synchronous method is <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent">GetEvent</a>. The asynchronous methods are <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent">BeginGetEvent</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">EndGetEvent</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-event-generators">Media Event Generators</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

