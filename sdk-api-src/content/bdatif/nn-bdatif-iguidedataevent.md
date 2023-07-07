---
UID: NN:bdatif.IGuideDataEvent
title: IGuideDataEvent (bdatif.h)
description: The IGuideDataEvent interface is used to receive events from the BDA MPEG-2 Transport Information Filter (TIF).This interface is an outgoing connection-point interface.
helpviewer_keywords: ["IGuideDataEvent","IGuideDataEvent interface [Microsoft TV Technologies]","IGuideDataEvent interface [Microsoft TV Technologies]","described","IGuideDataEventInterface","bdatif/IGuideDataEvent","mstv.iguidedataevent"]
old-location: mstv\iguidedataevent.htm
tech.root: mstv
ms.assetid: 9da565f2-fbcb-4d71-ae40-7d9821f46630
ms.date: 12/05/2018
ms.keywords: IGuideDataEvent, IGuideDataEvent interface [Microsoft TV Technologies], IGuideDataEvent interface [Microsoft TV Technologies],described, IGuideDataEventInterface, bdatif/IGuideDataEvent, mstv.iguidedataevent
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGuideDataEvent
 - bdatif/IGuideDataEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - IGuideDataEvent
---

# IGuideDataEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IGuideDataEvent</b> interface is used to receive events from the <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> (TIF).

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection. The event sink must not block the calling thread. If the client requires additional information about the event, it should make calls on a separate thread.

## -inheritance

The <b>IGuideDataEvent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGuideDataEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IGuideDataEvent)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
