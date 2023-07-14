---
UID: NF:tuner.IATSCChannelTuneRequest.get_MinorChannel
title: IATSCChannelTuneRequest::get_MinorChannel (tuner.h)
description: The get_MinorChannel method gets the current minor channel.
helpviewer_keywords: ["IATSCChannelTuneRequest interface [Microsoft TV Technologies]","get_MinorChannel method","IATSCChannelTuneRequest.get_MinorChannel","IATSCChannelTuneRequest::get_MinorChannel","IATSCChannelTuneRequestget_MinorChannel","get_MinorChannel","get_MinorChannel method [Microsoft TV Technologies]","get_MinorChannel method [Microsoft TV Technologies]","IATSCChannelTuneRequest interface","mstv.iatscchanneltunerequest_get_minorchannel","tuner/IATSCChannelTuneRequest::get_MinorChannel"]
old-location: mstv\iatscchanneltunerequest_get_minorchannel.htm
tech.root: mstv
ms.assetid: 2b8aa006-faba-472b-836b-0ff1ae134232
ms.date: 12/05/2018
ms.keywords: IATSCChannelTuneRequest interface [Microsoft TV Technologies],get_MinorChannel method, IATSCChannelTuneRequest.get_MinorChannel, IATSCChannelTuneRequest::get_MinorChannel, IATSCChannelTuneRequestget_MinorChannel, get_MinorChannel, get_MinorChannel method [Microsoft TV Technologies], get_MinorChannel method [Microsoft TV Technologies],IATSCChannelTuneRequest interface, mstv.iatscchanneltunerequest_get_minorchannel, tuner/IATSCChannelTuneRequest::get_MinorChannel
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
 - IATSCChannelTuneRequest::get_MinorChannel
 - tuner/IATSCChannelTuneRequest::get_MinorChannel
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
 - IATSCChannelTuneRequest.get_MinorChannel
---

# IATSCChannelTuneRequest::get_MinorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MinorChannel</b> method gets the current minor channel.

## -parameters

### -param MinorChannel [out]

Receives the current minor channel. If the value received is -1, the tuner should tune to the first valid minor channel it finds.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest Interface</a>