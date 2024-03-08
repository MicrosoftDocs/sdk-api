---
UID: NN:segment.IMSVidStreamBufferRecordingControl
title: IMSVidStreamBufferRecordingControl (segment.h)
description: The IMSVidStreamBufferRecordingControl interface enables an application to manage a stream buffer recording object through the Video Control.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl","IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","described","IMSVidStreamBufferRecordingControlInterface","mstv.imsvidstreambufferrecordingcontrol","segment/IMSVidStreamBufferRecordingControl"]
old-location: mstv\imsvidstreambufferrecordingcontrol.htm
tech.root: mstv
ms.assetid: a61414dc-a9a0-4c65-8f5a-eaabc79783e3
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl, IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies], IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],described, IMSVidStreamBufferRecordingControlInterface, mstv.imsvidstreambufferrecordingcontrol, segment/IMSVidStreamBufferRecordingControl
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMSVidStreamBufferRecordingControl
 - segment/IMSVidStreamBufferRecordingControl
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
 - IMSVidStreamBufferRecordingControl
---

# IMSVidStreamBufferRecordingControl interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidStreamBufferRecordingControl</b> interface enables an application to manage a stream buffer recording object through the Video Control. To obtain this interface, call one of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_contentrecorder">IMSVidStreamBufferSink::get_ContentRecorder</a>
</li>
<li>
<a href="/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_referencerecorder">IMSVidStreamBufferSink::get_ReferenceRecorder</a>
</li>
</ul>

## -inheritance

The <b>IMSVidStreamBufferRecordingControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidStreamBufferRecordingControl</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferRecordingControl)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
