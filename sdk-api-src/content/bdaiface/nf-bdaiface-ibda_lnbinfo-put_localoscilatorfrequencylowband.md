---
UID: NF:bdaiface.IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand
title: IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand (bdaiface.h)
description: The put_LocalOscilatorFrequencyLowBand method specifies the frequency of the local oscillator's low band.
helpviewer_keywords: ["IBDA_LNBInfo interface [Microsoft TV Technologies]","put_LocalOscilatorFrequencyLowBand method","IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand","IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand","IBDA_LNBInfoput_LocalOscilatorFrequencyLowBand","bdaiface/IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand","mstv.ibda_lnbinfo_put_localoscilatorfrequencylowband","put_LocalOscilatorFrequencyLowBand","put_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies]","put_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies]","IBDA_LNBInfo interface"]
old-location: mstv\ibda_lnbinfo_put_localoscilatorfrequencylowband.htm
tech.root: mstv
ms.assetid: e1ba4cf7-f9d4-4cac-921f-19f34fd968fe
ms.date: 12/05/2018
ms.keywords: IBDA_LNBInfo interface [Microsoft TV Technologies],put_LocalOscilatorFrequencyLowBand method, IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand, IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand, IBDA_LNBInfoput_LocalOscilatorFrequencyLowBand, bdaiface/IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand, mstv.ibda_lnbinfo_put_localoscilatorfrequencylowband, put_LocalOscilatorFrequencyLowBand, put_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies], put_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies],IBDA_LNBInfo interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand
 - bdaiface/IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand
---

# IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_LocalOscilatorFrequencyLowBand</b> method specifies the frequency of the local oscillator's low band.

## -parameters

### -param ulLOFLow [in]

Specifies the low band frequency. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_lnbinfo">IBDA_LNBInfo Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-get_localoscilatorfrequencylowband">IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand</a>