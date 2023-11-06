---
UID: NF:segment.IMSVidAnalogTuner.ChannelAvailable
title: IMSVidAnalogTuner::ChannelAvailable (segment.h)
description: The ChannelAvailable method queries whether a specified channel is available for viewing.
helpviewer_keywords: ["ChannelAvailable","ChannelAvailable method [Microsoft TV Technologies]","ChannelAvailable method [Microsoft TV Technologies]","IMSVidAnalogTuner interface","IMSVidAnalogTuner interface [Microsoft TV Technologies]","ChannelAvailable method","IMSVidAnalogTuner.ChannelAvailable","IMSVidAnalogTuner::ChannelAvailable","IMSVidAnalogTunerChannelAvailable","mstv.imsvidanalogtuner_channelavailable","segment/IMSVidAnalogTuner::ChannelAvailable"]
old-location: mstv\imsvidanalogtuner_channelavailable.htm
tech.root: mstv
ms.assetid: 67533d80-6026-434f-a20f-ded3c119d318
ms.date: 12/05/2018
ms.keywords: ChannelAvailable, ChannelAvailable method [Microsoft TV Technologies], ChannelAvailable method [Microsoft TV Technologies],IMSVidAnalogTuner interface, IMSVidAnalogTuner interface [Microsoft TV Technologies],ChannelAvailable method, IMSVidAnalogTuner.ChannelAvailable, IMSVidAnalogTuner::ChannelAvailable, IMSVidAnalogTunerChannelAvailable, mstv.imsvidanalogtuner_channelavailable, segment/IMSVidAnalogTuner::ChannelAvailable
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
 - IMSVidAnalogTuner::ChannelAvailable
 - segment/IMSVidAnalogTuner::ChannelAvailable
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
 - IMSVidAnalogTuner.ChannelAvailable
---

# IMSVidAnalogTuner::ChannelAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ChannelAvailable</b> method queries whether a specified channel is available for viewing.

This method is currently not supported.

## -parameters

### -param nChannel [in]

Integer containing the channel.

### -param SignalStrength [in, out]

Pointer to a <b>long</b> value that specifies the signal strength.

### -param fSignalPresent [out]

Receives a <b>VARIANT_BOOL</b> that indicates whether a signal is present.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nf-strmif-iamtuner-signalpresent">IAMTuner::SignalPresent</a>



<a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner Interface</a>