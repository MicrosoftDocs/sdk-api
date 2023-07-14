---
UID: NN:segment.IMSVidStreamBufferSinkEvent4
title: IMSVidStreamBufferSinkEvent4 (segment.h)
description: The IMSVidStreamBufferSinkEvent4 interface receives events from the MSVidStreamBufferSink object.
helpviewer_keywords: ["IMSVidStreamBufferSinkEvent4","IMSVidStreamBufferSinkEvent4 interface [Microsoft TV Technologies]","IMSVidStreamBufferSinkEvent4 interface [Microsoft TV Technologies]","described","mstv.imsvidstreambuffersinkevent4","segment/IMSVidStreamBufferSinkEvent4"]
old-location: mstv\imsvidstreambuffersinkevent4.htm
tech.root: mstv
ms.assetid: afec7f7a-0c5b-47ca-b442-5dbdba54a7af
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSinkEvent4, IMSVidStreamBufferSinkEvent4 interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent4 interface [Microsoft TV Technologies],described, mstv.imsvidstreambuffersinkevent4, segment/IMSVidStreamBufferSinkEvent4
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
 - IMSVidStreamBufferSinkEvent4
 - segment/IMSVidStreamBufferSinkEvent4
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
 - IMSVidStreamBufferSinkEvent4
---

# IMSVidStreamBufferSinkEvent4 interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent">IMSVidStreamBufferSinkEvent4</a> interface receives events from the <a href="/previous-versions/windows/desktop/legacy/dd695135(v=vs.85)">MSVidStreamBufferSink</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.

## -inheritance

The <b>IMSVidStreamBufferSinkEvent4</b> interface inherits from <a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent3">IMSVidStreamBufferSinkEvent3</a>. <b>IMSVidStreamBufferSinkEvent4</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent4)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent3">IMSVidStreamBufferSinkEvent3</a>



<a href="/previous-versions/windows/desktop/legacy/dd695135(v=vs.85)">MSVidStreamBufferSink</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
