---
UID: NF:tuner.IDigitalCableTuneRequest.get_MajorChannel
title: IDigitalCableTuneRequest::get_MajorChannel (tuner.h)
description: The get_MajorChannel method retrieves the major channel number.
helpviewer_keywords: ["IDigitalCableTuneRequest interface [Microsoft TV Technologies]","get_MajorChannel method","IDigitalCableTuneRequest.get_MajorChannel","IDigitalCableTuneRequest::get_MajorChannel","IDigitalCableTuneRequestget_MajorChannel","get_MajorChannel","get_MajorChannel method [Microsoft TV Technologies]","get_MajorChannel method [Microsoft TV Technologies]","IDigitalCableTuneRequest interface","mstv.idigitalcabletunerequest_get_majorchannel","tuner/IDigitalCableTuneRequest::get_MajorChannel"]
old-location: mstv\idigitalcabletunerequest_get_majorchannel.htm
tech.root: mstv
ms.assetid: f8c59c66-1c86-4cfd-b295-ac1d1a75af17
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuneRequest interface [Microsoft TV Technologies],get_MajorChannel method, IDigitalCableTuneRequest.get_MajorChannel, IDigitalCableTuneRequest::get_MajorChannel, IDigitalCableTuneRequestget_MajorChannel, get_MajorChannel, get_MajorChannel method [Microsoft TV Technologies], get_MajorChannel method [Microsoft TV Technologies],IDigitalCableTuneRequest interface, mstv.idigitalcabletunerequest_get_majorchannel, tuner/IDigitalCableTuneRequest::get_MajorChannel
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IDigitalCableTuneRequest::get_MajorChannel
 - tuner/IDigitalCableTuneRequest::get_MajorChannel
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
 - IDigitalCableTuneRequest.get_MajorChannel
---

# IDigitalCableTuneRequest::get_MajorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MajorChannel</b> method retrieves the major channel number.

## -parameters

### -param pMajorChannel [out]

Receives the major channel number. If the value received is BDA_UNDEFINED_CHANNEL, the major channel number is not used.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitalcabletunerequest">IDigitalCableTuneRequest Interface</a>