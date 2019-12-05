---
UID: NN:mfidl.IMFMediaStream
title: IMFMediaStream (mfidl.h)
description: Represents one stream in a media source.
old-location: mf\imfmediastream.htm
tech.root: medfound
ms.assetid: 66d07292-3bfe-4e68-b26f-890996262b98
ms.date: 12/05/2018
ms.keywords: 66d07292-3bfe-4e68-b26f-890996262b98, IMFMediaStream, IMFMediaStream interface [Media Foundation], IMFMediaStream interface [Media Foundation],described, mf.imfmediastream, mfidl/IMFMediaStream
ms.topic: interface
f1_keywords:
- mfidl/IMFMediaStream
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
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
- IMFMediaStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaStream interface


## -description


Represents one stream in a media source.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>. <b>IMFMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-getmediasource">GetMediaSource</a>
</td>
<td align="left" width="63%">
Returns a pointer to the media source that created this media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-getstreamdescriptor">GetStreamDescriptor</a>
</td>
<td align="left" width="63%">
Returns the stream descriptor for this media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/remoterequestsample">RemoteRequestSample</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample">RequestSample</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample">RequestSample</a>
</td>
<td align="left" width="63%">
Requests a sample from the media source.

</td>
</tr>
</table> 


## -remarks



Streams are created when a media source is started. For each stream, the media source sends an <a href="https://docs.microsoft.com/windows/desktop/medfound/menewstream">MENewStream</a> event with a pointer to the stream's <b>IMFMediaStream</b> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-sources">Media Sources</a>
 

 

