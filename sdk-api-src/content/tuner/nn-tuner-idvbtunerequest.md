---
UID: NN:tuner.IDVBTuneRequest
title: IDVBTuneRequest (tuner.h)
description: The IDVBTuneRequest interface is implemented on the DVBTuneRequest object.
helpviewer_keywords: ["IDVBTuneRequest","IDVBTuneRequest interface [Microsoft TV Technologies]","IDVBTuneRequest interface [Microsoft TV Technologies]","described","IDVBTuneRequestInterface","mstv.idvbtunerequest","tuner/IDVBTuneRequest"]
old-location: mstv\idvbtunerequest.htm
tech.root: mstv
ms.assetid: 4d519bbc-38e1-47ce-bd73-a3eb1ea399d6
ms.date: 12/05/2018
ms.keywords: IDVBTuneRequest, IDVBTuneRequest interface [Microsoft TV Technologies], IDVBTuneRequest interface [Microsoft TV Technologies],described, IDVBTuneRequestInterface, mstv.idvbtunerequest, tuner/IDVBTuneRequest
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
 - IDVBTuneRequest
 - tuner/IDVBTuneRequest
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
 - IDVBTuneRequest
---

# IDVBTuneRequest interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IDVBTuneRequest</b> interface is implemented on the <a href="/previous-versions/windows/desktop/mstv/dvbtunerequest-object">DVBTuneRequest</a> object. It provides methods for acquiring a transport stream, and a service on that stream, in tuning spaces with a DVB network type. This information is obtained by the Guide Store loader from the TIF, stored in the tune request, and ultimately used by the Network Provider to configure the MPEG-2 Demultiplexer so that the correct packets are decoded and passed on to the downstream filters.

## -inheritance

The <b>IDVBTuneRequest</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>. <b>IDVBTuneRequest</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTuneRequest)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
