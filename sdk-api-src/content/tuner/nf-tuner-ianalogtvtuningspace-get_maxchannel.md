---
UID: NF:tuner.IAnalogTVTuningSpace.get_MaxChannel
title: IAnalogTVTuningSpace::get_MaxChannel (tuner.h)
description: The get_MaxChannel method gets the highest channel number for this tuning space.
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","get_MaxChannel method","IAnalogTVTuningSpace.get_MaxChannel","IAnalogTVTuningSpace::get_MaxChannel","IAnalogTVTuningSpaceget_MaxChannel","get_MaxChannel","get_MaxChannel method [Microsoft TV Technologies]","get_MaxChannel method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","mstv.ianalogtvtuningspace_get_maxchannel","tuner/IAnalogTVTuningSpace::get_MaxChannel"]
old-location: mstv\ianalogtvtuningspace_get_maxchannel.htm
tech.root: mstv
ms.assetid: e6ac3789-1989-4331-ad00-6720f4503bb7
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],get_MaxChannel method, IAnalogTVTuningSpace.get_MaxChannel, IAnalogTVTuningSpace::get_MaxChannel, IAnalogTVTuningSpaceget_MaxChannel, get_MaxChannel, get_MaxChannel method [Microsoft TV Technologies], get_MaxChannel method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, mstv.ianalogtvtuningspace_get_maxchannel, tuner/IAnalogTVTuningSpace::get_MaxChannel
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
 - IAnalogTVTuningSpace::get_MaxChannel
 - tuner/IAnalogTVTuningSpace::get_MaxChannel
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
 - IAnalogTVTuningSpace.get_MaxChannel
---

# IAnalogTVTuningSpace::get_MaxChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MaxChannel</b> method gets the highest channel number for this tuning space.

## -parameters

### -param MaxChannelVal [out]

Receives the highest channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

For example, an NTSC tuning space connected to an antenna would return 69.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>