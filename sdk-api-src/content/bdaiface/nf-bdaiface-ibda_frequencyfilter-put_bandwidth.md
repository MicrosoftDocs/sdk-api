---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_Bandwidth
title: IBDA_FrequencyFilter::put_Bandwidth
author: windows-sdk-content
description: The put_Bandwidth method specifies the bandwidth.
old-location: mstv\ibda_frequencyfilter_put_bandwidth.htm
tech.root: mstv
ms.assetid: 8e44a5b4-c3ea-4afa-aab3-4f6732a3bd82
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],put_Bandwidth method, IBDA_FrequencyFilter.put_Bandwidth, IBDA_FrequencyFilter::put_Bandwidth, IBDA_FrequencyFilterput_Bandwidth, bdaiface/IBDA_FrequencyFilter::put_Bandwidth, mstv.ibda_frequencyfilter_put_bandwidth, put_Bandwidth, put_Bandwidth method [Microsoft TV Technologies], put_Bandwidth method [Microsoft TV Technologies],IBDA_FrequencyFilter interface
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_FrequencyFilter.put_Bandwidth
: 
---

# IBDA_FrequencyFilter::put_Bandwidth


## -description



The <b>put_Bandwidth</b> method specifies the bandwidth.




## -parameters




### -param ulBandwidth [in]

Specifies the bandwidth. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd693359(v=VS.85).aspx">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693355(v=VS.85).aspx">IBDA_FrequencyFilter Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693357(v=VS.85).aspx">IBDA_FrequencyFilter::get_Bandwidth</a>
 

 

