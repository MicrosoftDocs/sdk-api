---
UID: NF:tuner.IAnalogTVTuningSpace.put_MaxChannel
title: IAnalogTVTuningSpace::put_MaxChannel (tuner.h)
description: The put_MaxChannel method sets the highest channel number for this tuning space.
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","put_MaxChannel method","IAnalogTVTuningSpace.put_MaxChannel","IAnalogTVTuningSpace::put_MaxChannel","IAnalogTVTuningSpaceput_MaxChannel","mstv.ianalogtvtuningspace_put_maxchannel","put_MaxChannel","put_MaxChannel method [Microsoft TV Technologies]","put_MaxChannel method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","tuner/IAnalogTVTuningSpace::put_MaxChannel"]
old-location: mstv\ianalogtvtuningspace_put_maxchannel.htm
tech.root: mstv
ms.assetid: 2a559069-0d8a-4904-b0de-0573b4c0d273
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],put_MaxChannel method, IAnalogTVTuningSpace.put_MaxChannel, IAnalogTVTuningSpace::put_MaxChannel, IAnalogTVTuningSpaceput_MaxChannel, mstv.ianalogtvtuningspace_put_maxchannel, put_MaxChannel, put_MaxChannel method [Microsoft TV Technologies], put_MaxChannel method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, tuner/IAnalogTVTuningSpace::put_MaxChannel
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
 - IAnalogTVTuningSpace::put_MaxChannel
 - tuner/IAnalogTVTuningSpace::put_MaxChannel
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
 - IAnalogTVTuningSpace.put_MaxChannel
---

# IAnalogTVTuningSpace::put_MaxChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MaxChannel</b> method sets the highest channel number for this tuning space.

## -parameters

### -param NewMaxChannelVal [in]

The highest channel number.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>