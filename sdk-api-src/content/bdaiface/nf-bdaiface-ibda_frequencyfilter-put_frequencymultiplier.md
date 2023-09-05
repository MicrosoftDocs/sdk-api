---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_FrequencyMultiplier
title: IBDA_FrequencyFilter::put_FrequencyMultiplier (bdaiface.h)
description: The put_FrequencyMultiplier method specifies the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).
helpviewer_keywords: ["IBDA_FrequencyFilter interface [Microsoft TV Technologies]","put_FrequencyMultiplier method","IBDA_FrequencyFilter.put_FrequencyMultiplier","IBDA_FrequencyFilter::put_FrequencyMultiplier","IBDA_FrequencyFilterput_FrequencyMultiplier","bdaiface/IBDA_FrequencyFilter::put_FrequencyMultiplier","mstv.ibda_frequencyfilter_put_frequencymultiplier","put_FrequencyMultiplier","put_FrequencyMultiplier method [Microsoft TV Technologies]","put_FrequencyMultiplier method [Microsoft TV Technologies]","IBDA_FrequencyFilter interface"]
old-location: mstv\ibda_frequencyfilter_put_frequencymultiplier.htm
tech.root: mstv
ms.assetid: b67bd442-26cf-4104-906c-e9510b99ad90
ms.date: 12/05/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],put_FrequencyMultiplier method, IBDA_FrequencyFilter.put_FrequencyMultiplier, IBDA_FrequencyFilter::put_FrequencyMultiplier, IBDA_FrequencyFilterput_FrequencyMultiplier, bdaiface/IBDA_FrequencyFilter::put_FrequencyMultiplier, mstv.ibda_frequencyfilter_put_frequencymultiplier, put_FrequencyMultiplier, put_FrequencyMultiplier method [Microsoft TV Technologies], put_FrequencyMultiplier method [Microsoft TV Technologies],IBDA_FrequencyFilter interface
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
 - IBDA_FrequencyFilter::put_FrequencyMultiplier
 - bdaiface/IBDA_FrequencyFilter::put_FrequencyMultiplier
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
 - IBDA_FrequencyFilter.put_FrequencyMultiplier
---

# IBDA_FrequencyFilter::put_FrequencyMultiplier


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_FrequencyMultiplier</b> method specifies the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).

## -parameters

### -param ulMultiplier [in]

Specifies the multiplier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Since frequencies for DVB-S, DVB-T, and ATSC should all be expressed in kilohertz, the default frequency multiplier should never be changed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_frequencyfilter">IBDA_FrequencyFilter Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_frequency">IBDA_FrequencyFilter::put_Frequency</a>