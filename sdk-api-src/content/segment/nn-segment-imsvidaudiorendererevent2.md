---
UID: NN:segment.IMSVidAudioRendererEvent2
title: IMSVidAudioRendererEvent2 (segment.h)
description: Implements an event system for the audio renderer associated with a Video Control.
helpviewer_keywords: ["IMSVidAudioRendererEvent2","IMSVidAudioRendererEvent2 interface [Microsoft TV Technologies]","IMSVidAudioRendererEvent2 interface [Microsoft TV Technologies]","described","mstv.imsvidaudiorendererevent2","segment/IMSVidAudioRendererEvent2"]
old-location: mstv\imsvidaudiorendererevent2.htm
tech.root: mstv
ms.assetid: f37d3abb-e8ad-4aae-884a-1c6c4fa445e2
ms.date: 12/05/2018
ms.keywords: IMSVidAudioRendererEvent2, IMSVidAudioRendererEvent2 interface [Microsoft TV Technologies], IMSVidAudioRendererEvent2 interface [Microsoft TV Technologies],described, mstv.imsvidaudiorendererevent2, segment/IMSVidAudioRendererEvent2
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidAudioRendererEvent2
 - segment/IMSVidAudioRendererEvent2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAudioRendererEvent2
---

# IMSVidAudioRendererEvent2 interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements an event system for the audio renderer associated with a Video Control. Audio renderer events are triggered by events from the audio decoder upstream of the audio renderer in the filter graph. 

The audio renderer subscribes to audio decoder events by using the <a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-registerforevent">ICodecAPI::RegisterForEvent</a> method. Each method in <b>IMSVidAudioRendererEvent2</b> corresponds to a codec property, as follows:
<ol>
<li>An audio decoder property changes.</li>
<li>The decoder fires an <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> event. The event data includes the GUID that identifies the codec property.</li>
<li>The audio renderer fires the corresponding <b>IMSVidAudioRendererEvent2</b> event.</li>
</ol>For a list of codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

## -inheritance

The <b>IMSVidAudioRendererEvent2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidaudiorendererevent">IMSVidAudioRendererEvent</a>. <b>IMSVidAudioRendererEvent2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAudioRendererEvent2)</code>.
