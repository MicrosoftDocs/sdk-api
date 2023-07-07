---
UID: NN:tuner.IATSCChannelTuneRequest
title: IATSCChannelTuneRequest (tuner.h)
description: The IATSCChannelTuneRequest interface provides methods for tuning to a channel in an ATSC network. The ATSCChannelTuneRequest object implements this interface.
helpviewer_keywords: ["IATSCChannelTuneRequest","IATSCChannelTuneRequest interface [Microsoft TV Technologies]","IATSCChannelTuneRequest interface [Microsoft TV Technologies]","described","IATSCChannelTuneRequestInterface","mstv.iatscchanneltunerequest","tuner/IATSCChannelTuneRequest"]
old-location: mstv\iatscchanneltunerequest.htm
tech.root: mstv
ms.assetid: 9b55e181-ae03-473c-a85a-f169744d911d
ms.date: 12/05/2018
ms.keywords: IATSCChannelTuneRequest, IATSCChannelTuneRequest interface [Microsoft TV Technologies], IATSCChannelTuneRequest interface [Microsoft TV Technologies],described, IATSCChannelTuneRequestInterface, mstv.iatscchanneltunerequest, tuner/IATSCChannelTuneRequest
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IATSCChannelTuneRequest
 - tuner/IATSCChannelTuneRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IATSCChannelTuneRequest
---

# IATSCChannelTuneRequest interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IATSCChannelTuneRequest</b> interface provides methods for tuning to a channel in an ATSC network. The <a href="/previous-versions/windows/desktop/mstv/atscchanneltunerequest-object">ATSCChannelTuneRequest</a> object implements this interface.

## -inheritance

The <b>IATSCChannelTuneRequest</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ichanneltunerequest">IChannelTuneRequest</a>. <b>IATSCChannelTuneRequest</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

ATSC defines a tune request in terms of a <i>major channel</i> and a <i>minor channel</i>. The major channel is mapped to a physical frequency and the minor channel identifies different programs within the same major channel. To access the channel numbers, use the following methods:

<ul>
<li>Major channel: <ul>
<li>
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ichanneltunerequest-get_channel">IChannelTuneRequest::get_Channel</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ichanneltunerequest-put_channel">IChannelTuneRequest::put_Channel</a>
</li>
</ul>
</li>
<li>Minor channel: <ul>
<li>
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatscchanneltunerequest-get_minorchannel">IATSCChannelTuneRequest::get_MinorChannel</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatscchanneltunerequest-put_minorchannel">IATSCChannelTuneRequest::put_MinorChannel</a>
</li>
</ul>
</li>
</ul>
To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCChannelTuneRequest)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ichanneltunerequest">IChannelTuneRequest</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
