---
UID: NF:bdaiface.IBDA_FrequencyFilter.get_Range
title: IBDA_FrequencyFilter::get_Range (bdaiface.h)
description: The get_Range method retrieves the tuner range. The tuner range is the frequency domain on which to find a particular carrier frequency.
helpviewer_keywords: ["IBDA_FrequencyFilter interface [Microsoft TV Technologies]","get_Range method","IBDA_FrequencyFilter.get_Range","IBDA_FrequencyFilter::get_Range","IBDA_FrequencyFilterget_Range","bdaiface/IBDA_FrequencyFilter::get_Range","get_Range","get_Range method [Microsoft TV Technologies]","get_Range method [Microsoft TV Technologies]","IBDA_FrequencyFilter interface","mstv.ibda_frequencyfilter_get_range"]
old-location: mstv\ibda_frequencyfilter_get_range.htm
tech.root: mstv
ms.assetid: fdf96400-8fd9-4989-9977-026a9bec37ea
ms.date: 12/05/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],get_Range method, IBDA_FrequencyFilter.get_Range, IBDA_FrequencyFilter::get_Range, IBDA_FrequencyFilterget_Range, bdaiface/IBDA_FrequencyFilter::get_Range, get_Range, get_Range method [Microsoft TV Technologies], get_Range method [Microsoft TV Technologies],IBDA_FrequencyFilter interface, mstv.ibda_frequencyfilter_get_range
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
 - IBDA_FrequencyFilter::get_Range
 - bdaiface/IBDA_FrequencyFilter::get_Range
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
 - IBDA_FrequencyFilter.get_Range
---

# IBDA_FrequencyFilter::get_Range


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The get_Range method retrieves the tuner range. The <i>tuner range</i> is the frequency domain on which to find a particular carrier frequency

## -parameters

### -param pulRange [out]

Pointer that receives the tuner range. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz). A value of -1 for this parameter indicates that the tuner range is not set. A value of 0 for this parameter indicates that  the tuner range is undefined.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_frequencyfilter">IBDA_FrequencyFilter Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_range">IBDA_FrequencyFilter::put_Range</a>