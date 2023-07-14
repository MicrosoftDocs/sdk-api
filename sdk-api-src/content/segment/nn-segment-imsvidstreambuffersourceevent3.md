---
UID: NN:segment.IMSVidStreamBufferSourceEvent3
title: IMSVidStreamBufferSourceEvent3 (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent3","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","described","IMSVidStreamBufferSourceEvent3Interface","mstv.imsvidstreambuffersourceevent3","segment/IMSVidStreamBufferSourceEvent3"]
old-location: mstv\imsvidstreambuffersourceevent3.htm
tech.root: mstv
ms.assetid: 4ff2e05f-1c26-48f2-8c46-beebb8b0b1b3
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent3, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies], IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceEvent3Interface, mstv.imsvidstreambuffersourceevent3, segment/IMSVidStreamBufferSourceEvent3
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMSVidStreamBufferSourceEvent3
 - segment/IMSVidStreamBufferSourceEvent3
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
 - IMSVidStreamBufferSourceEvent3
---

# IMSVidStreamBufferSourceEvent3 interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSourceEvent3</b> interface is used to receive events from the <a href="/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.

## -inheritance

The <b>IMSVidStreamBufferSourceEvent3</b> interface inherits from <a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent2">IMSVidStreamBufferSourceEvent2</a>. <b>IMSVidStreamBufferSourceEvent3</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSourceEvent3)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent2">IMSVidStreamBufferSourceEvent2</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
