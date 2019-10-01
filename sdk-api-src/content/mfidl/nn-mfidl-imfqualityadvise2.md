---
UID: NN:mfidl.IMFQualityAdvise2
title: IMFQualityAdvise2 (mfidl.h)
author: windows-sdk-content
description: Enables a pipeline object to adjust its own audio or video quality, in response to quality messages.
old-location: mf\imfqualityadvise2.htm
tech.root: medfound
ms.assetid: c6114bbc-31d8-45eb-9bf8-745b3138dd50
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFQualityAdvise2, IMFQualityAdvise2 interface [Media Foundation], IMFQualityAdvise2 interface [Media Foundation],described, mf.imfqualityadvise2, mfidl/IMFQualityAdvise2
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFQualityAdvise2"
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - IMFQualityAdvise2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFQualityAdvise2 interface


## -description


Enables a pipeline object to adjust its own audio or video quality, in response to quality messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFQualityAdvise2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>. <b>IMFQualityAdvise2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFQualityAdvise2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise2-notifyqualityevent">NotifyQualityEvent</a>
</td>
<td align="left" width="63%">
Forwards an <a href="https://docs.microsoft.com/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> event from the media sink.

</td>
</tr>
</table> 


## -remarks



This interface enables a pipeline object to respond to quality messages from the media sink. Currently, it is supported only for video decoders.

If a video decoder exposes <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a> but not <b>IMFQualityAdvise2</b>, the quality manager controls quality adjustments for the decoder. In this case, the quality manager responds to <a href="https://docs.microsoft.com/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> events from the Enhanced Video Renderer (EVR) by calling <b>IMFQualityAdvise</b> methods on the decoder.

If the decoder exposes <b>IMFQualityAdvise2</b>, the quality manager forwards the <a href="https://docs.microsoft.com/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> events to the decoder and does not adjust the decoder's quality settings. The decoder should respond to these events by adjusting its own quality settings internally.

The preceding remarks apply to the default implementation of the quality manager; custom quality managers can implement other behaviors.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

