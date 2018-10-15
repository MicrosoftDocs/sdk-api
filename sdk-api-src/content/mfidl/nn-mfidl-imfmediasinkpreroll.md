---
UID: NN:mfidl.IMFMediaSinkPreroll
title: IMFMediaSinkPreroll
author: windows-sdk-content
description: Enables a media sink to receive samples before the presentation clock is started.
old-location: mf\imfmediasinkpreroll.htm
tech.root: medfound
ms.assetid: 7cc93751-4477-4649-b09e-53f519fb1acb
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 7cc93751-4477-4649-b09e-53f519fb1acb, IMFMediaSinkPreroll, IMFMediaSinkPreroll interface [Media Foundation], IMFMediaSinkPreroll interface [Media Foundation],described, mf.imfmediasinkpreroll, mfidl/IMFMediaSinkPreroll
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMFMediaSinkPreroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSinkPreroll interface


## -description


Enables a media sink to receive samples before the presentation clock is started.

To get a pointer to this interface, call <b>QueryInterface</b> on the media sink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSinkPreroll</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaSinkPreroll</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSinkPreroll</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0694ad9-a18a-4fea-a9ff-b416bd4827ba">NotifyPreroll</a>
</td>
<td align="left" width="63%">
Notifies the media sink that the presentation clock is about to start.

</td>
</tr>
</table> 


## -remarks



Media sinks can implement this interface to support seamless playback and transitions. If a media sink exposes this interface, it can receive samples before the presentation clock starts. It can then pre-process the samples, so that rendering can begin immediately when the clock starts. Prerolling helps to avoid glitches during playback.

If a media sink supports preroll, the media sink's <a href="https://msdn.microsoft.com/a7e8e2af-8b10-47f5-8b09-a7147ace5ba1">IMFMediaSink::GetCharacteristics</a> method should return the MEDIASINK_CAN_PREROLL flag.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

