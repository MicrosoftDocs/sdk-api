---
UID: NF:tuner.IDigitalCableTuneRequest.get_SourceID
title: IDigitalCableTuneRequest::get_SourceID (tuner.h)
description: The get_SourceID method retrieves the source identifier, which maps to a physical channel.
helpviewer_keywords: ["IDigitalCableTuneRequest interface [Microsoft TV Technologies]","get_SourceID method","IDigitalCableTuneRequest.get_SourceID","IDigitalCableTuneRequest::get_SourceID","IDigitalCableTuneRequestget_SourceID","get_SourceID","get_SourceID method [Microsoft TV Technologies]","get_SourceID method [Microsoft TV Technologies]","IDigitalCableTuneRequest interface","mstv.idigitalcabletunerequest_get_sourceid","tuner/IDigitalCableTuneRequest::get_SourceID"]
old-location: mstv\idigitalcabletunerequest_get_sourceid.htm
tech.root: mstv
ms.assetid: 3767a8b4-f318-4242-9b30-f1293b3f7091
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuneRequest interface [Microsoft TV Technologies],get_SourceID method, IDigitalCableTuneRequest.get_SourceID, IDigitalCableTuneRequest::get_SourceID, IDigitalCableTuneRequestget_SourceID, get_SourceID, get_SourceID method [Microsoft TV Technologies], get_SourceID method [Microsoft TV Technologies],IDigitalCableTuneRequest interface, mstv.idigitalcabletunerequest_get_sourceid, tuner/IDigitalCableTuneRequest::get_SourceID
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
 - IDigitalCableTuneRequest::get_SourceID
 - tuner/IDigitalCableTuneRequest::get_SourceID
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
 - IDigitalCableTuneRequest.get_SourceID
---

# IDigitalCableTuneRequest::get_SourceID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SourceID</b> method retrieves the source identifier, which maps to a physical channel.

## -parameters

### -param pSourceID [out]

Receives the source identifier. If the value received is BDA_UNDEFINED_CHANNEL, the source identifier is not used.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitalcabletunerequest">IDigitalCableTuneRequest Interface</a>