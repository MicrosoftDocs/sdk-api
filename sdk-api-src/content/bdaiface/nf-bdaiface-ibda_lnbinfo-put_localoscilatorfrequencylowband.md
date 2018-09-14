---
UID: NF:bdaiface.IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand
title: IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand
author: windows-sdk-content
description: The put_LocalOscilatorFrequencyLowBand method specifies the frequency of the local oscillator's low band.
old-location: mstv\ibda_lnbinfo_put_localoscilatorfrequencylowband.htm
tech.root: MSTV
ms.assetid: e1ba4cf7-f9d4-4cac-921f-19f34fd968fe
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IBDA_LNBInfo interface [Microsoft TV Technologies],put_LocalOscilatorFrequencyLowBand method, IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand, IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand, IBDA_LNBInfoput_LocalOscilatorFrequencyLowBand, bdaiface/IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand, mstv.ibda_lnbinfo_put_localoscilatorfrequencylowband, put_LocalOscilatorFrequencyLowBand, put_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies], put_LocalOscilatorFrequencyLowBand method [Microsoft TV Technologies],IBDA_LNBInfo interface
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
 - IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_LNBInfo::put_LocalOscilatorFrequencyLowBand


## -description



The <b>put_LocalOscilatorFrequencyLowBand</b> method specifies the frequency of the local oscillator's low band.




## -parameters




### -param ulLOFLow [in]

Specifies the low band frequency. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd693359(v=VS.85).aspx">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693396(v=VS.85).aspx">IBDA_LNBInfo Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693399(v=VS.85).aspx">IBDA_LNBInfo::get_LocalOscilatorFrequencyLowBand</a>
 

 

