---
UID: NF:tuner.IChannelTuneRequest.get_Channel
title: IChannelTuneRequest::get_Channel (tuner.h)
description: The get_Channel method gets the channel to be tuned.
helpviewer_keywords: ["IChannelTuneRequest interface [Microsoft TV Technologies]","get_Channel method","IChannelTuneRequest.get_Channel","IChannelTuneRequest::get_Channel","IChannelTuneRequestget_Channel","get_Channel","get_Channel method [Microsoft TV Technologies]","get_Channel method [Microsoft TV Technologies]","IChannelTuneRequest interface","mstv.ichanneltunerequest_get_channel","tuner/IChannelTuneRequest::get_Channel"]
old-location: mstv\ichanneltunerequest_get_channel.htm
tech.root: mstv
ms.assetid: 1a529416-9b7a-41f4-961a-741b1a581d5f
ms.date: 12/05/2018
ms.keywords: IChannelTuneRequest interface [Microsoft TV Technologies],get_Channel method, IChannelTuneRequest.get_Channel, IChannelTuneRequest::get_Channel, IChannelTuneRequestget_Channel, get_Channel, get_Channel method [Microsoft TV Technologies], get_Channel method [Microsoft TV Technologies],IChannelTuneRequest interface, mstv.ichanneltunerequest_get_channel, tuner/IChannelTuneRequest::get_Channel
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
 - IChannelTuneRequest::get_Channel
 - tuner/IChannelTuneRequest::get_Channel
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
 - IChannelTuneRequest.get_Channel
---

# IChannelTuneRequest::get_Channel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Channel</b> method gets the channel to be tuned.

## -parameters

### -param Channel [out]

Pointer to a variable of type <b>long</b> that receives the current channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ichanneltunerequest">IChannelTuneRequest Interface</a>