---
UID: NN:tuner.IMPEG2TuneRequestSupport
title: IMPEG2TuneRequestSupport
description: Indicates that the default network provider for a tuning space allows tuning through the IMPEG2TuneRequest interface as well as tuning through the native tuning request type implemented by that tuning space's CreateTuneRequest method.
helpviewer_keywords: ["IMPEG2TuneRequestSupport","IMPEG2TuneRequestSupport interface [Microsoft TV Technologies]","IMPEG2TuneRequestSupport interface [Microsoft TV Technologies]","described","mstv.impeg2tunerequestsupport","tuner/IMPEG2TuneRequestSupport"]
old-location: mstv\impeg2tunerequestsupport.htm
tech.root: mstv
ms.assetid: 22ba436f-8ccf-4f78-b33c-2328bd495df6
ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequestSupport, IMPEG2TuneRequestSupport interface [Microsoft TV Technologies], IMPEG2TuneRequestSupport interface [Microsoft TV Technologies],described, mstv.impeg2tunerequestsupport, tuner/IMPEG2TuneRequestSupport
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
f1_keywords:
 - IMPEG2TuneRequestSupport
 - tuner/IMPEG2TuneRequestSupport
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
 - IMPEG2TuneRequestSupport
---

# IMPEG2TuneRequestSupport interface


## -description

Indicates that the default network provider for a tuning space allows tuning through the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2tunerequest">IMPEG2TuneRequest</a> interface as well as tuning through the native tuning request type implemented by that tuning space's <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-createtunerequest">CreateTuneRequest</a> method.

For example, the <a href="/previous-versions/windows/desktop/mstv/dvbtuningspace-object">DVBTuningSpace</a> object implements the <b>IMPEG2TuneRequestSupport</b> interface. This indicates that the default network provider for the <b>DVBTuningSpace</b> object supports tuning through both the object's native <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-createtunerequest">IDVBTuneRequest::CreateTuneRequest</a> method and the <b>IMPEG2TuneRequest::CreateTuneRequest</b> method. (In both cases, the tune request interfaces inherit the <b>CreateTuneRequest</b> method from the  <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequest</a> interface).

The following tuning space objects support the <b>IMPEG2TuneRequestSupport</b> interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/mstv/dvbstuningspace-object">DVBSTuningSpace</a> object</li>
<li>
<a href="/previous-versions/windows/desktop/mstv/dvbtuningspace-object">DVBTuningSpace</a> object</li>
<li>
<a href="/previous-versions/windows/desktop/mstv/atsctuningspace-object">ATSCTuningSpace</a> object</li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestSupport)</code>.