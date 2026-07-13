---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_Autotune
title: IBDA_FrequencyFilter::put_Autotune (bdaiface.h)
description: The put_Autotune method specifies whether to activate the device's autotune capabilities.
helpviewer_keywords: ["IBDA_FrequencyFilter interface [Microsoft TV Technologies]","put_Autotune method","IBDA_FrequencyFilter.put_Autotune","IBDA_FrequencyFilter::put_Autotune","IBDA_FrequencyFilterput_Autotune","bdaiface/IBDA_FrequencyFilter::put_Autotune","mstv.ibda_frequencyfilter_put_autotune","put_Autotune","put_Autotune method [Microsoft TV Technologies]","put_Autotune method [Microsoft TV Technologies]","IBDA_FrequencyFilter interface"]
old-location: mstv\ibda_frequencyfilter_put_autotune.htm
tech.root: mstv
ms.assetid: e2ca03b8-fd22-4b8f-90a9-42a235b0a675
ms.date: 12/05/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],put_Autotune method, IBDA_FrequencyFilter.put_Autotune, IBDA_FrequencyFilter::put_Autotune, IBDA_FrequencyFilterput_Autotune, bdaiface/IBDA_FrequencyFilter::put_Autotune, mstv.ibda_frequencyfilter_put_autotune, put_Autotune, put_Autotune method [Microsoft TV Technologies], put_Autotune method [Microsoft TV Technologies],IBDA_FrequencyFilter interface
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
 - IBDA_FrequencyFilter::put_Autotune
 - bdaiface/IBDA_FrequencyFilter::put_Autotune
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
 - IBDA_FrequencyFilter.put_Autotune
---

# IBDA_FrequencyFilter::put_Autotune


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Autotune</b> method specifies whether to activate the device's autotune capabilities.

## -parameters

### -param ulTransponder [in]

Specifies the transponder frequency.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_frequencyfilter">IBDA_FrequencyFilter Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_autotune">IBDA_FrequencyFilter::get_Autotune</a>