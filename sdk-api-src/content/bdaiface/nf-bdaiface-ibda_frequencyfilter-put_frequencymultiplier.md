---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_FrequencyMultiplier
title: IBDA_FrequencyFilter::put_FrequencyMultiplier method
author: windows-driver-content
description: The put_FrequencyMultiplier method specifies the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).
old-location: mstv\ibda_frequencyfilter_put_frequencymultiplier.htm
old-project: mstv
ms.assetid: b67bd442-26cf-4104-906c-e9510b99ad90
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IBDA_FrequencyFilter, IBDA_FrequencyFilter interface [Microsoft TV Technologies], put_FrequencyMultiplier method, IBDA_FrequencyFilter::put_FrequencyMultiplier, IBDA_FrequencyFilterput_FrequencyMultiplier, bdaiface/IBDA_FrequencyFilter::put_FrequencyMultiplier, mstv.ibda_frequencyfilter_put_frequencymultiplier, put_FrequencyMultiplier method [Microsoft TV Technologies], put_FrequencyMultiplier method [Microsoft TV Technologies], IBDA_FrequencyFilter interface, put_FrequencyMultiplier,IBDA_FrequencyFilter.put_FrequencyMultiplier
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
-	IBDA_FrequencyFilter.put_FrequencyMultiplier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_FrequencyFilter::put_FrequencyMultiplier method


## -description



The <b>put_FrequencyMultiplier</b> method specifies the frequency multiplier. The frequency multiplier determines the frequency units for the methods on this interface. The default value is 1000, meaning that frequencies are expressed in kilohertz (kHz).




## -parameters




### -param ulMultiplier [in]

Specifies the multiplier.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Since fequencies for DVB-S, DVB-T, and ATSC should all be expressed in kilohertz, the default frequency multiplier should never be changed.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ef5dbf4a-ecbb-4f2c-a34d-ce3864133adc">IBDA_FrequencyFilter Interface</a>



<a href="https://msdn.microsoft.com/463a58f7-a10c-40b5-8183-3e16bcc7c6b2">IBDA_FrequencyFilter::get_FrequencyMultiplier</a>



<a href="https://msdn.microsoft.com/70d50a4b-b0f8-42a1-9fa2-1d09376903fe">IBDA_FrequencyFilter::put_Frequency</a>
 

 

