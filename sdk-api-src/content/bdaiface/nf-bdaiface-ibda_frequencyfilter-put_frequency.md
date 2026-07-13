---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_Frequency
title: IBDA_FrequencyFilter::put_Frequency (bdaiface.h)
description: The put_Frequency method specifies the frequency.
helpviewer_keywords: ["IBDA_FrequencyFilter interface [Microsoft TV Technologies]","put_Frequency method","IBDA_FrequencyFilter.put_Frequency","IBDA_FrequencyFilter::put_Frequency","IBDA_FrequencyFilterput_Frequency","bdaiface/IBDA_FrequencyFilter::put_Frequency","mstv.ibda_frequencyfilter_put_frequency","put_Frequency","put_Frequency method [Microsoft TV Technologies]","put_Frequency method [Microsoft TV Technologies]","IBDA_FrequencyFilter interface"]
old-location: mstv\ibda_frequencyfilter_put_frequency.htm
tech.root: mstv
ms.assetid: 70d50a4b-b0f8-42a1-9fa2-1d09376903fe
ms.date: 12/05/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],put_Frequency method, IBDA_FrequencyFilter.put_Frequency, IBDA_FrequencyFilter::put_Frequency, IBDA_FrequencyFilterput_Frequency, bdaiface/IBDA_FrequencyFilter::put_Frequency, mstv.ibda_frequencyfilter_put_frequency, put_Frequency, put_Frequency method [Microsoft TV Technologies], put_Frequency method [Microsoft TV Technologies],IBDA_FrequencyFilter interface
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
 - IBDA_FrequencyFilter::put_Frequency
 - bdaiface/IBDA_FrequencyFilter::put_Frequency
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
 - IBDA_FrequencyFilter.put_Frequency
---

# IBDA_FrequencyFilter::put_Frequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Frequency</b> method specifies the frequency.

## -parameters

### -param ulFrequency [in]

Specifies the frequency. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Frequencies for DVB-S, DVB-T, and ATSC should all be expressed in kilohertz and therefore the default frequency multiplier should not be changed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_frequencyfilter">IBDA_FrequencyFilter Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequency">IBDA_FrequencyFilter::get_Frequency</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_frequencymultiplier">IBDA_FrequencyFilter::put_FrequencyMultiplier</a>