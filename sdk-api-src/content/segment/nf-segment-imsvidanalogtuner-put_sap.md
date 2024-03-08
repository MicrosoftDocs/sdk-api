---
UID: NF:segment.IMSVidAnalogTuner.put_SAP
title: IMSVidAnalogTuner::put_SAP (segment.h)
description: The put_SAP method specifies the tuner's SAP setting to enable secondary audio components.
helpviewer_keywords: ["IMSVidAnalogTuner interface [Microsoft TV Technologies]","put_SAP method","IMSVidAnalogTuner.put_SAP","IMSVidAnalogTuner::put_SAP","IMSVidAnalogTunerput_SAP","mstv.imsvidanalogtuner_put_sap","put_SAP","put_SAP method [Microsoft TV Technologies]","put_SAP method [Microsoft TV Technologies]","IMSVidAnalogTuner interface","segment/IMSVidAnalogTuner::put_SAP"]
old-location: mstv\imsvidanalogtuner_put_sap.htm
tech.root: mstv
ms.assetid: e27efb36-de0c-4255-a5d8-6357f283cd12
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],put_SAP method, IMSVidAnalogTuner.put_SAP, IMSVidAnalogTuner::put_SAP, IMSVidAnalogTunerput_SAP, mstv.imsvidanalogtuner_put_sap, put_SAP, put_SAP method [Microsoft TV Technologies], put_SAP method [Microsoft TV Technologies],IMSVidAnalogTuner interface, segment/IMSVidAnalogTuner::put_SAP
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidAnalogTuner::put_SAP
 - segment/IMSVidAnalogTuner::put_SAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAnalogTuner.put_SAP
---

# IMSVidAnalogTuner::put_SAP


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SAP</b> method specifies the tuner's SAP setting to enable secondary audio components.

This method is currently not supported.

## -parameters

### -param fSapOn [in]

Flag indicating whether to enable or disable SAP.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio Interface</a>



<a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidanalogtuner-get_sap">IMSVidAnalogTuner::get_SAP</a>