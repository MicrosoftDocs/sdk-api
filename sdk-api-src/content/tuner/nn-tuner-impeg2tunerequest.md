---
UID: NN:tuner.IMPEG2TuneRequest
title: IMPEG2TuneRequest (tuner.h)
description: The IMPEG2TuneRequest interface represents a tune request for a basic MPEG-2 transport stream containing the minimal tables.Use the IMPEG2TuneRequestFactory::CreateTuneRequest method to obtain this interface.
helpviewer_keywords: ["IMPEG2TuneRequest","IMPEG2TuneRequest interface [Microsoft TV Technologies]","IMPEG2TuneRequest interface [Microsoft TV Technologies]","described","IMPEG2TuneRequestInterface","mstv.impeg2tunerequest","tuner/IMPEG2TuneRequest"]
old-location: mstv\impeg2tunerequest.htm
tech.root: mstv
ms.assetid: a9e37b8b-9272-43c6-b36e-1e82b0d1b0db
ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequest, IMPEG2TuneRequest interface [Microsoft TV Technologies], IMPEG2TuneRequest interface [Microsoft TV Technologies],described, IMPEG2TuneRequestInterface, mstv.impeg2tunerequest, tuner/IMPEG2TuneRequest
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
 - IMPEG2TuneRequest
 - tuner/IMPEG2TuneRequest
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
 - IMPEG2TuneRequest
---

# IMPEG2TuneRequest interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMPEG2TuneRequest</b> interface represents a tune request for a basic MPEG-2 transport stream containing the minimal tables.

Use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2tunerequestfactory-createtunerequest">IMPEG2TuneRequestFactory::CreateTuneRequest</a> method to obtain this interface. It returns the minimal MPEG-2 tune request for a specified tuning space. To create a full tune request, use the <b>CreateTuneRequest</b> method provided by one of the tuning space objects.

## -inheritance

The <b>IMPEG2TuneRequest</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>. <b>IMPEG2TuneRequest</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequest)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
