---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_Bandwidth
title: IBDA_FrequencyFilter::put_Bandwidth (bdaiface.h)
author: windows-sdk-content
description: The put_Bandwidth method specifies the bandwidth.
old-location: mstv\ibda_frequencyfilter_put_bandwidth.htm
tech.root: mstv
ms.assetid: 8e44a5b4-c3ea-4afa-aab3-4f6732a3bd82
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],put_Bandwidth method, IBDA_FrequencyFilter.put_Bandwidth, IBDA_FrequencyFilter::put_Bandwidth, IBDA_FrequencyFilterput_Bandwidth, bdaiface/IBDA_FrequencyFilter::put_Bandwidth, mstv.ibda_frequencyfilter_put_bandwidth, put_Bandwidth, put_Bandwidth method [Microsoft TV Technologies], put_Bandwidth method [Microsoft TV Technologies],IBDA_FrequencyFilter interface
ms.topic: method
f1_keywords: 
 - "bdaiface/IBDA_FrequencyFilter.put_Bandwidth"
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
 - IBDA_FrequencyFilter.put_Bandwidth
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_FrequencyFilter::put_Bandwidth


## -description



The <b>put_Bandwidth</b> method specifies the bandwidth.




## -parameters




### -param ulBandwidth [in]

Specifies the bandwidth. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_frequencyfilter">IBDA_FrequencyFilter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_bandwidth">IBDA_FrequencyFilter::get_Bandwidth</a>
 

 

