---
UID: NF:bdaiface.IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand
title: IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand
author: windows-sdk-content
description: The get_LocalOscilatorFrequencyLowBand method retrieves the low band of the local oscillator frequency.
old-location: mstv\ibda_lnbinfo_get_localoscilatorfrequencylowband.htm
old-project: mstv
ms.assetid: 8aabb13a-166f-4b50-90a5-a18dd4b04720
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_LNBInfo interface [Microsoft TV Technologies],get_LocalOscilatorFrequencyLowBand method, IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand, IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand, IBDA_LNBInfoget_LocalOscilatorFrequencyLowBand, bdaiface/IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand, get_LocalOscilatorFrequencyLowBand, get_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies], get_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies],IBDA_LNBInfo interface, mstv.ibda_lnbinfo_get_localoscilatorfrequencylowband
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
 - IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand


## -description



The <b>get_LocalOscilatorFrequencyLowBand</b> method retrieves the low band of the local oscillator frequency.




## -parameters




### -param pulLOFLow [out]

Pointer that receives the low band of the frequency. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/463a58f7-a10c-40b5-8183-3e16bcc7c6b2">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4985b525-c000-4d19-9679-c995cbc3c99b">IBDA_LNBInfo Interface</a>



<a href="https://msdn.microsoft.com/e1ba4cf7-f9d4-4cac-921f-19f34fd968fe">IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand</a>
 

 

