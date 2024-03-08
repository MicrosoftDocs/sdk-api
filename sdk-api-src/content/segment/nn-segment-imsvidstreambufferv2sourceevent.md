---
UID: NN:segment.IMSVidStreamBufferV2SourceEvent
title: IMSVidStreamBufferV2SourceEvent (segment.h)
description: Implements an event system for the Stream Buffer Engine, version 2 (SBE2) source filter that is wrapped in the Video Control. Each event corresponds to an event that the SBE2 source filter receives inside a DirectShow graph.
helpviewer_keywords: ["IMSVidStreamBufferV2SourceEvent","IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","described","mstv.imsvidstreambufferv2sourceevent","segment/IMSVidStreamBufferV2SourceEvent"]
old-location: mstv\imsvidstreambufferv2sourceevent.htm
tech.root: mstv
ms.assetid: ab463f6e-0718-4420-89bc-28b3c447f3a0
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies], IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],described, mstv.imsvidstreambufferv2sourceevent, segment/IMSVidStreamBufferV2SourceEvent
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
 - IMSVidStreamBufferV2SourceEvent
 - segment/IMSVidStreamBufferV2SourceEvent
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
 - IMSVidStreamBufferV2SourceEvent
---

# IMSVidStreamBufferV2SourceEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements an event system for the Stream Buffer Engine, version 2 (SBE2) source filter that is wrapped in the Video Control. Each event corresponds to an event that the SBE2 source filter receives inside a DirectShow graph.

## -inheritance

The <b>IMSVidStreamBufferV2SourceEvent</b> interface inherits from <b>IMSVidFilePlaybackEvent</b>. <b>IMSVidStreamBufferV2SourceEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferV2SourceEvent)</code>.
