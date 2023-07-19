---
UID: NF:tuner.IAnalogTVTuningSpace.put_InputType
title: IAnalogTVTuningSpace::put_InputType (tuner.h)
description: The put_InputType method sets the input type (antenna or cable) intended for the tuning space.
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","put_InputType method","IAnalogTVTuningSpace.put_InputType","IAnalogTVTuningSpace::put_InputType","IAnalogTVTuningSpaceput_InputType","mstv.ianalogtvtuningspace_put_inputtype","put_InputType","put_InputType method [Microsoft TV Technologies]","put_InputType method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","tuner/IAnalogTVTuningSpace::put_InputType"]
old-location: mstv\ianalogtvtuningspace_put_inputtype.htm
tech.root: mstv
ms.assetid: 399503a2-60e9-4feb-ba69-cafef70b2540
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],put_InputType method, IAnalogTVTuningSpace.put_InputType, IAnalogTVTuningSpace::put_InputType, IAnalogTVTuningSpaceput_InputType, mstv.ianalogtvtuningspace_put_inputtype, put_InputType, put_InputType method [Microsoft TV Technologies], put_InputType method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, tuner/IAnalogTVTuningSpace::put_InputType
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
 - IAnalogTVTuningSpace::put_InputType
 - tuner/IAnalogTVTuningSpace::put_InputType
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
 - IAnalogTVTuningSpace.put_InputType
---

# IAnalogTVTuningSpace::put_InputType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_InputType</b> method sets the input type (antenna or cable) intended for the tuning space.

## -parameters

### -param NewInputTypeVal [in]

Variable of type <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-tunerinputtype">TunerInputType</a> that specifies the input type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>