---
UID: NF:bdaiface.IBDA_LNBInfo.get_HighLowSwitchFrequency
title: IBDA_LNBInfo::get_HighLowSwitchFrequency (bdaiface.h)
description: The get_HighLowSwitchFrequency method retrieves the frequency of the high-low switch.
helpviewer_keywords: ["IBDA_LNBInfo interface [Microsoft TV Technologies]","get_HighLowSwitchFrequency method","IBDA_LNBInfo.get_HighLowSwitchFrequency","IBDA_LNBInfo::get_HighLowSwitchFrequency","IBDA_LNBInfoget_HighLowSwitchFrequency","bdaiface/IBDA_LNBInfo::get_HighLowSwitchFrequency","get_HighLowSwitchFrequency","get_HighLowSwitchFrequency method [Microsoft TV Technologies]","get_HighLowSwitchFrequency method [Microsoft TV Technologies]","IBDA_LNBInfo interface","mstv.ibda_lnbinfo_get_highlowswitchfrequency"]
old-location: mstv\ibda_lnbinfo_get_highlowswitchfrequency.htm
tech.root: mstv
ms.assetid: f6a851fc-6911-41fb-951c-c9fcf04b2355
ms.date: 12/05/2018
ms.keywords: IBDA_LNBInfo interface [Microsoft TV Technologies],get_HighLowSwitchFrequency method, IBDA_LNBInfo.get_HighLowSwitchFrequency, IBDA_LNBInfo::get_HighLowSwitchFrequency, IBDA_LNBInfoget_HighLowSwitchFrequency, bdaiface/IBDA_LNBInfo::get_HighLowSwitchFrequency, get_HighLowSwitchFrequency, get_HighLowSwitchFrequency method [Microsoft TV Technologies], get_HighLowSwitchFrequency method [Microsoft TV Technologies],IBDA_LNBInfo interface, mstv.ibda_lnbinfo_get_highlowswitchfrequency
f1_keywords:
- bdaiface/IBDA_LNBInfo.get_HighLowSwitchFrequency
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- bdaiface.h
api_name:
- IBDA_LNBInfo.get_HighLowSwitchFrequency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_LNBInfo::get_HighLowSwitchFrequency


## -description



The <b>get_HighLowSwitchFrequency</b> method retrieves the frequency of the high-low switch.




## -parameters




### -param pulSwitchFrequency [in, out]

Pointer that receives the frequency. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_lnbinfo">IBDA_LNBInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-put_highlowswitchfrequency">IBDA_LNBInfo::put_HighLowSwitchFrequency</a>
 

 

