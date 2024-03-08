---
UID: NN:tuner.IChannelTuneRequest
title: IChannelTuneRequest (tuner.h)
description: The IChannelTuneRequest interface is implemented on tuning request objects that support channel numbers, including analog TV and ATSC.
helpviewer_keywords: ["IChannelTuneRequest","IChannelTuneRequest interface [Microsoft TV Technologies]","IChannelTuneRequest interface [Microsoft TV Technologies]","described","IChannelTuneRequestInterface","mstv.ichanneltunerequest","tuner/IChannelTuneRequest"]
old-location: mstv\ichanneltunerequest.htm
tech.root: mstv
ms.assetid: cdb65c1a-bd86-4dc8-a72f-c08e36999880
ms.date: 12/05/2018
ms.keywords: IChannelTuneRequest, IChannelTuneRequest interface [Microsoft TV Technologies], IChannelTuneRequest interface [Microsoft TV Technologies],described, IChannelTuneRequestInterface, mstv.ichanneltunerequest, tuner/IChannelTuneRequest
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
 - IChannelTuneRequest
 - tuner/IChannelTuneRequest
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
 - IChannelTuneRequest
---

# IChannelTuneRequest interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IChannelTuneRequest</b> interface is implemented on tuning request objects that support channel numbers, including analog TV and ATSC.

This interface enables a guide store loader running on Windows XP to create tuning requests for analog TV networks that an application can pass to the Video Control. The Video Control examines all tuning requests that it receives. If it is an analog tuning request, the Video Control creates a filter graph that can play the specified channel. Applications running on earlier versions of Windows are responsible for creating their own analog graphs if the user selects a program on an analog channel. Downlevel applications should not pass an analog tune request to a BDA tuning device because the device cannot interpret it.

## -inheritance

The <b>IChannelTuneRequest</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>. <b>IChannelTuneRequest</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IChannelTuneRequest)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
