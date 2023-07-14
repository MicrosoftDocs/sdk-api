---
UID: NF:bdaiface.IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand
title: IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand (bdaiface.h)
description: The get_LocalOscilatorFrequencyLowBand method retrieves the low band of the local oscillator frequency.
helpviewer_keywords: ["IBDA_LNBInfo interface [Microsoft TV Technologies]","get_LocalOscilatorFrequencyLowBand method","IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand","IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand","IBDA_LNBInfoget_LocalOscilatorFrequencyLowBand","bdaiface/IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand","get_LocalOscilatorFrequencyLowBand","get_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies]","get_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies]","IBDA_LNBInfo interface","mstv.ibda_lnbinfo_get_localoscilatorfrequencylowband"]
old-location: mstv\ibda_lnbinfo_get_localoscilatorfrequencylowband.htm
tech.root: mstv
ms.assetid: 8aabb13a-166f-4b50-90a5-a18dd4b04720
ms.date: 12/05/2018
ms.keywords: IBDA_LNBInfo interface [Microsoft TV Technologies],get_LocalOscilatorFrequencyLowBand method, IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand, IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand, IBDA_LNBInfoget_LocalOscilatorFrequencyLowBand, bdaiface/IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand, get_LocalOscilatorFrequencyLowBand, get_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies], get_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies],IBDA_LNBInfo interface, mstv.ibda_lnbinfo_get_localoscilatorfrequencylowband
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
 - IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand
 - bdaiface/IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand
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
 - IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand
---

# IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_LocalOscilatorFrequencyLowBand</b> method retrieves the low band of the local oscillator frequency.

## -parameters

### -param pulLOFLow [out]

Pointer that receives the low band of the frequency. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_lnbinfo">IBDA_LNBInfo Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-put_localoscilatorfrequencylowband">IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand</a>