---
UID: NN:evr.IMFVideoPresenter
title: IMFVideoPresenter (evr.h)
author: windows-sdk-content
description: Represents a video presenter. A video presenter is an object that receives video frames, typically from a video mixer, and presents them in some way, typically by rendering them to the display.
old-location: mf\imfvideopresenter.htm
tech.root: medfound
ms.assetid: 8f6e3132-03e9-4a2e-9160-e39d29cf2408
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 8f6e3132-03e9-4a2e-9160-e39d29cf2408, IMFVideoPresenter, IMFVideoPresenter interface [Media Foundation], IMFVideoPresenter interface [Media Foundation],described, evr/IMFVideoPresenter, mf.imfvideopresenter
ms.topic: interface
f1_keywords: 
 - "evr/IMFVideoPresenter"
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPresenter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoPresenter interface


## -description


Represents a video presenter. A <i>video presenter</i> is an object that receives video frames, typically from a video mixer, and presents them in some way, typically by rendering them to the display. The enhanced video renderer (EVR) provides a default video presenter, and applications can implement custom presenters.

The video presenter receives video frames as soon as they are available from upstream. The video presenter is responsible for presenting frames at the correct time and for synchronizing with the presentation clock.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoPresenter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>. <b>IMFVideoPresenter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype">GetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the presenter's media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage">ProcessMessage</a>
</td>
<td align="left" width="63%">
Sends a message to the video presenter.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

