---
UID: NN:tuner.IMPEG2TuneRequestSupport~r1
title: IMPEG2TuneRequestSupport
description: TBD
helpviewer_keywords: ["- IMPEG2TuneRequestSupport"]
tech.root: mstv
ms.assetid: b7381962-b76e-4041-a080-66408d0f3cb7
ms.date: 11/14/2019
req.header: tuner.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - IMPEG2TuneRequestSupport
 - tuner/IMPEG2TuneRequestSupport
dev_langs:
 - c++
topic_type:
 - apiref
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

## -inheritance

IMPEG2TuneRequestSupport inherits from .

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestSupport)</code>.

## -see-also
