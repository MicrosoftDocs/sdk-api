---
UID: NN:evr.IEVRFilterConfig
title: IEVRFilterConfig (evr.h)

description: Sets the number of input pins on the DirectShow Enhanced Video Renderer (EVR) filter.
old-location: mf\ievrfilterconfig.htm
tech.root: medfound
ms.assetid: 13086d85-3dbf-4e9f-b065-d95e16412832

ms.date: 12/05/2018
ms.keywords: 13086d85-3dbf-4e9f-b065-d95e16412832, IEVRFilterConfig, IEVRFilterConfig interface [Media Foundation], IEVRFilterConfig interface [Media Foundation],described, evr/IEVRFilterConfig, mf.ievrfilterconfig
ms.topic: interface
f1_keywords: 
 - "evr/IEVRFilterConfig"
dev_langs:
 - c++
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
 - IEVRFilterConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEVRFilterConfig interface


## -description


Sets the number of input pins on the DirectShow <a href="https://docs.microsoft.com/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer</a> (EVR) filter. To get a pointer to this interface, call <b>QueryInterface</b> on the DirectShow EVR filter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEVRFilterConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEVRFilterConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEVRFilterConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-ievrfilterconfig-getnumberofstreams">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Retrieves the number of input pins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams">SetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Sets the number of input pins.

</td>
</tr>
</table> 


## -remarks



The DirectShow EVR filter starts with one input pin, which corresponds to the reference stream. To create additional pins for video substreams, call <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams">SetNumberOfStreams</a>.

The EVR media sink for Media Foundation does not support this interface. To add new streams to the EVR media sink, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

