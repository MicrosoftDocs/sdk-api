---
UID: NN:mfidl.IMFMediaSink
title: IMFMediaSink (mfidl.h)
description: Implemented by media sink objects.
old-location: mf\imfmediasink.htm
tech.root: medfound
ms.assetid: 103e6fd8-a18f-480a-8261-099623014659
ms.date: 12/05/2018
ms.keywords: 103e6fd8-a18f-480a-8261-099623014659, IMFMediaSink, IMFMediaSink interface [Media Foundation], IMFMediaSink interface [Media Foundation],described, mf.imfmediasink, mfidl/IMFMediaSink
f1_keywords:
- mfidl/IMFMediaSink
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
- IMFMediaSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSink interface


## -description


Implemented by media sink objects. This interface is the base interface for all Media Foundation media sinks. Stream sinks handle the actual processing of data on each stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">AddStreamSink</a>
</td>
<td align="left" width="63%">
Adds a new stream sink to the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Gets the characteristics of the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getpresentationclock">GetPresentationClock</a>
</td>
<td align="left" width="63%">
Gets the presentation clock that was set on the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid">GetStreamSinkById</a>
</td>
<td align="left" width="63%">
Gets a stream sink, specified by stream identifier.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex">GetStreamSinkByIndex</a>
</td>
<td align="left" width="63%">
Gets a stream sink, specified by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount">GetStreamSinkCount</a>
</td>
<td align="left" width="63%">
Gets the number of stream sinks on this media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink">RemoveStreamSink</a>
</td>
<td align="left" width="63%">
Removes a stream sink from the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock">SetPresentationClock</a>
</td>
<td align="left" width="63%">
Sets the presentation clock on the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the media sink and releases the resources it is using.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-sinks">Media Sinks</a>
 

 

