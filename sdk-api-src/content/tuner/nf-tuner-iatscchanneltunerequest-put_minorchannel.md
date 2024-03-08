---
UID: NF:tuner.IATSCChannelTuneRequest.put_MinorChannel
title: IATSCChannelTuneRequest::put_MinorChannel (tuner.h)
description: The put_MinorChannel method sets the minor channel to be tuned.
helpviewer_keywords: ["IATSCChannelTuneRequest interface [Microsoft TV Technologies]","put_MinorChannel method","IATSCChannelTuneRequest.put_MinorChannel","IATSCChannelTuneRequest::put_MinorChannel","IATSCChannelTuneRequestput_MinorChannel","mstv.iatscchanneltunerequest_put_minorchannel","put_MinorChannel","put_MinorChannel method [Microsoft TV Technologies]","put_MinorChannel method [Microsoft TV Technologies]","IATSCChannelTuneRequest interface","tuner/IATSCChannelTuneRequest::put_MinorChannel"]
old-location: mstv\iatscchanneltunerequest_put_minorchannel.htm
tech.root: mstv
ms.assetid: 1288d249-58de-410e-852b-233133f56da5
ms.date: 12/05/2018
ms.keywords: IATSCChannelTuneRequest interface [Microsoft TV Technologies],put_MinorChannel method, IATSCChannelTuneRequest.put_MinorChannel, IATSCChannelTuneRequest::put_MinorChannel, IATSCChannelTuneRequestput_MinorChannel, mstv.iatscchanneltunerequest_put_minorchannel, put_MinorChannel, put_MinorChannel method [Microsoft TV Technologies], put_MinorChannel method [Microsoft TV Technologies],IATSCChannelTuneRequest interface, tuner/IATSCChannelTuneRequest::put_MinorChannel
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
 - IATSCChannelTuneRequest::put_MinorChannel
 - tuner/IATSCChannelTuneRequest::put_MinorChannel
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
 - IATSCChannelTuneRequest.put_MinorChannel
---

# IATSCChannelTuneRequest::put_MinorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MinorChannel</b> method sets the minor channel to be tuned.

## -parameters

### -param MinorChannel [in]

Specifies the minor channel. If the value is -1, the tuner tunes to the first valid minor channel it finds.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest Interface</a>