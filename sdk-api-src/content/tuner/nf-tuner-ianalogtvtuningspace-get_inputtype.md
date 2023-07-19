---
UID: NF:tuner.IAnalogTVTuningSpace.get_InputType
title: IAnalogTVTuningSpace::get_InputType (tuner.h)
description: The get_InputType method gets the input type (antenna or cable) intended for the tuning space.
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","get_InputType method","IAnalogTVTuningSpace.get_InputType","IAnalogTVTuningSpace::get_InputType","IAnalogTVTuningSpaceget_InputType","get_InputType","get_InputType method [Microsoft TV Technologies]","get_InputType method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","mstv.ianalogtvtuningspace_get_inputtype","tuner/IAnalogTVTuningSpace::get_InputType"]
old-location: mstv\ianalogtvtuningspace_get_inputtype.htm
tech.root: mstv
ms.assetid: c016a61b-6b4f-4101-a357-38b8be754a57
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],get_InputType method, IAnalogTVTuningSpace.get_InputType, IAnalogTVTuningSpace::get_InputType, IAnalogTVTuningSpaceget_InputType, get_InputType, get_InputType method [Microsoft TV Technologies], get_InputType method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, mstv.ianalogtvtuningspace_get_inputtype, tuner/IAnalogTVTuningSpace::get_InputType
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
 - IAnalogTVTuningSpace::get_InputType
 - tuner/IAnalogTVTuningSpace::get_InputType
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
 - IAnalogTVTuningSpace.get_InputType
---

# IAnalogTVTuningSpace::get_InputType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_InputType</b> method gets the input type (antenna or cable) intended for the tuning space.

## -parameters

### -param InputTypeVal [out]

Pointer to a variable of type <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-tunerinputtype">TunerInputType</a> that receives the input type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>