---
UID: NN:tuner.IMPEG2TuneRequestFactory
title: IMPEG2TuneRequestFactory (tuner.h)
description: The IMPEG2TuneRequestFactory interface creates a tune request for a basic MPEG-2 transport stream containing the minimal tables. To obtain this interface, call CoCreateInstance with the class identifier CLSID_MPEG2TuneRequestFactory.
helpviewer_keywords: ["IMPEG2TuneRequestFactory","IMPEG2TuneRequestFactory interface [Microsoft TV Technologies]","IMPEG2TuneRequestFactory interface [Microsoft TV Technologies]","described","IMPEG2TuneRequestFactoryInterface","mstv.impeg2tunerequestfactory","tuner/IMPEG2TuneRequestFactory"]
old-location: mstv\impeg2tunerequestfactory.htm
tech.root: mstv
ms.assetid: 0fbeab7d-0c54-45e3-a73c-755df28a16d5
ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequestFactory, IMPEG2TuneRequestFactory interface [Microsoft TV Technologies], IMPEG2TuneRequestFactory interface [Microsoft TV Technologies],described, IMPEG2TuneRequestFactoryInterface, mstv.impeg2tunerequestfactory, tuner/IMPEG2TuneRequestFactory
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMPEG2TuneRequestFactory
 - tuner/IMPEG2TuneRequestFactory
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
 - IMPEG2TuneRequestFactory
---

# IMPEG2TuneRequestFactory interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMPEG2TuneRequestFactory</b> interface creates a tune request for a basic MPEG-2 transport stream containing the minimal tables. To obtain this interface, call <b>CoCreateInstance</b> with the class identifier CLSID_MPEG2TuneRequestFactory.

## -inheritance

The <b>IMPEG2TuneRequestFactory</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMPEG2TuneRequestFactory</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To create a full tune request, use the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ibdacreatetunerequestex">CreateTuneRequest</a> method provided by one of the tuning space objects.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestFactory)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
