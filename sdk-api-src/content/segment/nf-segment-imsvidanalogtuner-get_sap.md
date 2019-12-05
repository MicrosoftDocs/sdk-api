---
UID: NF:segment.IMSVidAnalogTuner.get_SAP
title: IMSVidAnalogTuner::get_SAP (segment.h)
description: The get_SAP method retrieves the tuner's SAP setting to enable secondary audio components.
old-location: mstv\imsvidanalogtuner_get_sap.htm
tech.root: mstv
ms.assetid: 9943ca7e-754e-4145-8f52-0a915fd7133d
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_SAP method, IMSVidAnalogTuner.get_SAP, IMSVidAnalogTuner::get_SAP, IMSVidAnalogTunerget_SAP, get_SAP, get_SAP method [Microsoft TV Technologies], get_SAP method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_sap, segment/IMSVidAnalogTuner::get_SAP
ms.topic: method
f1_keywords:
- segment/IMSVidAnalogTuner.get_SAP
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidAnalogTuner.get_SAP
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidAnalogTuner::get_SAP


## -description


The <b>get_SAP</b> method retrieves the tuner's SAP setting to enable secondary audio components.

This method is currently not supported.


## -parameters




### -param pfSapOn [out]

Pointer to a flag indicating whether SAP is on.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidanalogtuner-put_sap">IMSVidAnalogTuner::put_SAP</a>
 

 

