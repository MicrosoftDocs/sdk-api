---
UID: NF:bdaiface.IBDA_FrequencyFilter.get_Bandwidth
title: IBDA_FrequencyFilter::get_Bandwidth
author: windows-sdk-content
description: The get_Bandwidth method retrieves the bandwidth.
old-location: mstv\ibda_frequencyfilter_get_bandwidth.htm
old-project: mstv
ms.assetid: 3cea7bbe-488b-4c5c-84a8-28f0dc77e3c1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],get_Bandwidth method, IBDA_FrequencyFilter.get_Bandwidth, IBDA_FrequencyFilter::get_Bandwidth, IBDA_FrequencyFilterget_Bandwidth, bdaiface/IBDA_FrequencyFilter::get_Bandwidth, get_Bandwidth, get_Bandwidth method [Microsoft TV Technologies], get_Bandwidth method [Microsoft TV Technologies],IBDA_FrequencyFilter interface, mstv.ibda_frequencyfilter_get_bandwidth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_FrequencyFilter.get_Bandwidth
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_FrequencyFilter::get_Bandwidth


## -description



The <b>get_Bandwidth</b> method retrieves the bandwidth.




## -parameters




### -param pulBandwidth [out]

Pointer that receives the bandwidth. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/463a58f7-a10c-40b5-8183-3e16bcc7c6b2">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ef5dbf4a-ecbb-4f2c-a34d-ce3864133adc">IBDA_FrequencyFilter Interface</a>



<a href="https://msdn.microsoft.com/8e44a5b4-c3ea-4afa-aab3-4f6732a3bd82">IBDA_FrequencyFilter::put_Bandwidth</a>
 

 

