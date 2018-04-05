---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_Frequency
title: IBDA_FrequencyFilter::put_Frequency method
author: windows-driver-content
description: The put_Frequency method specifies the frequency.
old-location: mstv\ibda_frequencyfilter_put_frequency.htm
old-project: mstv
ms.assetid: 70d50a4b-b0f8-42a1-9fa2-1d09376903fe
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IBDA_FrequencyFilter, IBDA_FrequencyFilter interface [Microsoft TV Technologies], put_Frequency method, IBDA_FrequencyFilter::put_Frequency, IBDA_FrequencyFilterput_Frequency, bdaiface/IBDA_FrequencyFilter::put_Frequency, mstv.ibda_frequencyfilter_put_frequency, put_Frequency method [Microsoft TV Technologies], put_Frequency method [Microsoft TV Technologies], IBDA_FrequencyFilter interface, put_Frequency,IBDA_FrequencyFilter.put_Frequency
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_FrequencyFilter.put_Frequency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_FrequencyFilter::put_Frequency method


## -description



The <b>put_Frequency</b> method specifies the frequency.




## -parameters




### -param ulFrequency [in]

Specifies the frequency. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/463a58f7-a10c-40b5-8183-3e16bcc7c6b2">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Frequencies for DVB-S, DVB-T, and ATSC should all be expressed in kilohertz and therefore the default frequency multiplier should not be changed.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ef5dbf4a-ecbb-4f2c-a34d-ce3864133adc">IBDA_FrequencyFilter Interface</a>



<a href="https://msdn.microsoft.com/0eba0f92-45a7-4c5e-9450-f3c7a176288c">IBDA_FrequencyFilter::get_Frequency</a>



<a href="https://msdn.microsoft.com/b67bd442-26cf-4104-906c-e9510b99ad90">IBDA_FrequencyFilter::put_FrequencyMultiplier</a>
 

 

