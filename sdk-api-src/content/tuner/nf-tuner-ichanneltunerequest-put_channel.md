---
UID: NF:tuner.IChannelTuneRequest.put_Channel
title: IChannelTuneRequest::put_Channel (tuner.h)
description: The put_Channel method sets the channel to be tuned.
helpviewer_keywords: ["IChannelTuneRequest interface [Microsoft TV Technologies]","put_Channel method","IChannelTuneRequest.put_Channel","IChannelTuneRequest::put_Channel","IChannelTuneRequestput_Channel","mstv.ichanneltunerequest_put_channel","put_Channel","put_Channel method [Microsoft TV Technologies]","put_Channel method [Microsoft TV Technologies]","IChannelTuneRequest interface","tuner/IChannelTuneRequest::put_Channel"]
old-location: mstv\ichanneltunerequest_put_channel.htm
tech.root: mstv
ms.assetid: 67a08647-a2b5-43b2-b5d2-3917beb6dd27
ms.date: 12/05/2018
ms.keywords: IChannelTuneRequest interface [Microsoft TV Technologies],put_Channel method, IChannelTuneRequest.put_Channel, IChannelTuneRequest::put_Channel, IChannelTuneRequestput_Channel, mstv.ichanneltunerequest_put_channel, put_Channel, put_Channel method [Microsoft TV Technologies], put_Channel method [Microsoft TV Technologies],IChannelTuneRequest interface, tuner/IChannelTuneRequest::put_Channel
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
 - IChannelTuneRequest::put_Channel
 - tuner/IChannelTuneRequest::put_Channel
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
 - IChannelTuneRequest.put_Channel
---

# IChannelTuneRequest::put_Channel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Channel</b> method sets the channel to be tuned.

## -parameters

### -param Channel [in]

Variable of type <b>long</b> that specifies the channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM IErrorInfo interface.

## -remarks

If the value specified for <i>Channel</i> is less than the minimum channel set for the tuning space, it will "wrap around" to the maximum channel value. Likewise, if the value specified for <i>Channel</i> is greater than the maximum channel set for the tuning space, it will "wrap around" to the minimum channel value.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ichanneltunerequest">IChannelTuneRequest Interface</a>