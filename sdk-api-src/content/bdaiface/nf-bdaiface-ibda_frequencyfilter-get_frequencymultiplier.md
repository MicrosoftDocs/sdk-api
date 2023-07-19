---
UID: NF:bdaiface.IBDA_FrequencyFilter.get_FrequencyMultiplier
title: IBDA_FrequencyFilter::get_FrequencyMultiplier (bdaiface.h)
description: The get_FrequencyMultiplier method retrieves the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).
helpviewer_keywords: ["IBDA_FrequencyFilter interface [Microsoft TV Technologies]","get_FrequencyMultiplier method","IBDA_FrequencyFilter.get_FrequencyMultiplier","IBDA_FrequencyFilter::get_FrequencyMultiplier","IBDA_FrequencyFilterget_FrequencyMultiplier","bdaiface/IBDA_FrequencyFilter::get_FrequencyMultiplier","get_FrequencyMultiplier","get_FrequencyMultiplier method [Microsoft TV Technologies]","get_FrequencyMultiplier method [Microsoft TV Technologies]","IBDA_FrequencyFilter interface","mstv.ibda_frequencyfilter_get_frequencymultiplier"]
old-location: mstv\ibda_frequencyfilter_get_frequencymultiplier.htm
tech.root: mstv
ms.assetid: 463a58f7-a10c-40b5-8183-3e16bcc7c6b2
ms.date: 12/05/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],get_FrequencyMultiplier method, IBDA_FrequencyFilter.get_FrequencyMultiplier, IBDA_FrequencyFilter::get_FrequencyMultiplier, IBDA_FrequencyFilterget_FrequencyMultiplier, bdaiface/IBDA_FrequencyFilter::get_FrequencyMultiplier, get_FrequencyMultiplier, get_FrequencyMultiplier method [Microsoft TV Technologies], get_FrequencyMultiplier method [Microsoft TV Technologies],IBDA_FrequencyFilter interface, mstv.ibda_frequencyfilter_get_frequencymultiplier
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
 - IBDA_FrequencyFilter::get_FrequencyMultiplier
 - bdaiface/IBDA_FrequencyFilter::get_FrequencyMultiplier
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
 - IBDA_FrequencyFilter.get_FrequencyMultiplier
---

# IBDA_FrequencyFilter::get_FrequencyMultiplier


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_FrequencyMultiplier</b> method retrieves the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).

## -parameters

### -param pulMultiplier [out]

Pointer that receives the multiplier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Frequencies for DVB-S, DVB-T, and ATSC should all be expressed in kilohertz and therefore the default frequency multiplier should not be changed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_frequencyfilter">IBDA_FrequencyFilter Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequency">IBDA_FrequencyFilter::get_Frequency</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_frequencymultiplier">IBDA_FrequencyFilter::put_FrequencyMultiplier</a>