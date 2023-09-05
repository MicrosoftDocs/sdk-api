---
UID: NN:tuner.ITuneRequest
title: ITuneRequest (tuner.h)
description: The ITuneRequest interface is the base interface for all tune requests.
helpviewer_keywords: ["ITuneRequest","ITuneRequest interface [Microsoft TV Technologies]","ITuneRequest interface [Microsoft TV Technologies]","described","ITuneRequestInterface","mstv.itunerequest","tuner/ITuneRequest"]
old-location: mstv\itunerequest.htm
tech.root: mstv
ms.assetid: 34077b45-32b4-466b-b103-6a42fc869265
ms.date: 12/05/2018
ms.keywords: ITuneRequest, ITuneRequest interface [Microsoft TV Technologies], ITuneRequest interface [Microsoft TV Technologies],described, ITuneRequestInterface, mstv.itunerequest, tuner/ITuneRequest
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
 - ITuneRequest
 - tuner/ITuneRequest
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
 - ITuneRequest
---

# ITuneRequest interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ITuneRequest</b> interface is the base interface for all tune requests. Each tune request object supports a network-specific interface that derives from <b>ITuneRequest</b>, such as <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a> or <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest</a>.

This interface is used by any application that creates tune requests, such as a Guide Store loader. A tune request must be associated with a specific network type. When a tune request is submitted, the derived interfaces are used by the Network Provider to extract the tuning information required by the hardware. All tune request objects also support <b>IPersistPropertyBag</b>, which enables them to be persisted in some type of third-party storage mechanism.

## -inheritance

The <b>ITuneRequest</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITuneRequest</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuneRequest)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
