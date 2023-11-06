---
UID: NF:tuner.IAnalogTVTuningSpace.get_MinChannel
title: IAnalogTVTuningSpace::get_MinChannel (tuner.h)
description: The get_MinChannel method gets the lowest channel number for this tuning space.
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","get_MinChannel method","IAnalogTVTuningSpace.get_MinChannel","IAnalogTVTuningSpace::get_MinChannel","IAnalogTVTuningSpaceget_MinChannel","get_MinChannel","get_MinChannel method [Microsoft TV Technologies]","get_MinChannel method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","mstv.ianalogtvtuningspace_get_minchannel","tuner/IAnalogTVTuningSpace::get_MinChannel"]
old-location: mstv\ianalogtvtuningspace_get_minchannel.htm
tech.root: mstv
ms.assetid: 94c3136f-6d9e-4396-9bbf-828669d57724
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],get_MinChannel method, IAnalogTVTuningSpace.get_MinChannel, IAnalogTVTuningSpace::get_MinChannel, IAnalogTVTuningSpaceget_MinChannel, get_MinChannel, get_MinChannel method [Microsoft TV Technologies], get_MinChannel method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, mstv.ianalogtvtuningspace_get_minchannel, tuner/IAnalogTVTuningSpace::get_MinChannel
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
 - IAnalogTVTuningSpace::get_MinChannel
 - tuner/IAnalogTVTuningSpace::get_MinChannel
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
 - IAnalogTVTuningSpace.get_MinChannel
---

# IAnalogTVTuningSpace::get_MinChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MinChannel</b> method gets the lowest channel number for this tuning space.

## -parameters

### -param MinChannelVal [out]

Receives the lowest channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

An NTSC tuning space connected to an antenna will return a value of 2.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>