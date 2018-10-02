---
UID: NF:bdaiface.IBDA_FrequencyFilter.get_FrequencyMultiplier
title: IBDA_FrequencyFilter::get_FrequencyMultiplier
author: windows-sdk-content
description: The get_FrequencyMultiplier method retrieves the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).
old-location: mstv\ibda_frequencyfilter_get_frequencymultiplier.htm
tech.root: MSTV
ms.assetid: 463a58f7-a10c-40b5-8183-3e16bcc7c6b2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],get_FrequencyMultiplier method, IBDA_FrequencyFilter.get_FrequencyMultiplier, IBDA_FrequencyFilter::get_FrequencyMultiplier, IBDA_FrequencyFilterget_FrequencyMultiplier, bdaiface/IBDA_FrequencyFilter::get_FrequencyMultiplier, get_FrequencyMultiplier, get_FrequencyMultiplier method [Microsoft TV Technologies], get_FrequencyMultiplier method [Microsoft TV Technologies],IBDA_FrequencyFilter interface, mstv.ibda_frequencyfilter_get_frequencymultiplier
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
 - IBDA_FrequencyFilter.get_FrequencyMultiplier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_FrequencyFilter::get_FrequencyMultiplier


## -description



The <b>get_FrequencyMultiplier</b> method retrieves the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).




## -parameters




### -param pulMultiplier [out]

Pointer that receives the multiplier.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Frequencies for DVB-S, DVB-T, and ATSC should all be expressed in kilohertz and therefore the default frequency multiplier should not be changed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693355(v=VS.85).aspx">IBDA_FrequencyFilter Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693358(v=VS.85).aspx">IBDA_FrequencyFilter::get_Frequency</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693365(v=VS.85).aspx">IBDA_FrequencyFilter::put_FrequencyMultiplier</a>
 

 

