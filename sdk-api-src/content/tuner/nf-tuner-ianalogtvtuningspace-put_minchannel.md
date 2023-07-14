---
UID: NF:tuner.IAnalogTVTuningSpace.put_MinChannel
title: IAnalogTVTuningSpace::put_MinChannel (tuner.h)
description: The put_MinChannel method sets the lowest channel number for this tuning space.
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","put_MinChannel method","IAnalogTVTuningSpace.put_MinChannel","IAnalogTVTuningSpace::put_MinChannel","IAnalogTVTuningSpaceput_MinChannel","mstv.ianalogtvtuningspace_put_minchannel","put_MinChannel","put_MinChannel method [Microsoft TV Technologies]","put_MinChannel method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","tuner/IAnalogTVTuningSpace::put_MinChannel"]
old-location: mstv\ianalogtvtuningspace_put_minchannel.htm
tech.root: mstv
ms.assetid: e0e348a6-a536-4c1b-82ba-c2502c5d92c0
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],put_MinChannel method, IAnalogTVTuningSpace.put_MinChannel, IAnalogTVTuningSpace::put_MinChannel, IAnalogTVTuningSpaceput_MinChannel, mstv.ianalogtvtuningspace_put_minchannel, put_MinChannel, put_MinChannel method [Microsoft TV Technologies], put_MinChannel method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, tuner/IAnalogTVTuningSpace::put_MinChannel
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
 - IAnalogTVTuningSpace::put_MinChannel
 - tuner/IAnalogTVTuningSpace::put_MinChannel
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
 - IAnalogTVTuningSpace.put_MinChannel
---

# IAnalogTVTuningSpace::put_MinChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MinChannel</b> method sets the lowest channel number for this tuning space.

## -parameters

### -param NewMinChannelVal [in]

The lowest channel number.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>