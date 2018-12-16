---
UID: NF:bdaiface.IBDA_LNBInfo.get_LocalOscilatorFrequencyHighBand
title: IBDA_LNBInfo::get_LocalOscilatorFrequencyHighBand
author: windows-sdk-content
description: The get_LocalOscilatorFrequencyHighBand method retrieves the high band of the local oscillator frequency.
old-location: mstv\ibda_lnbinfo_get_localoscilatorfrequencyhighband.htm
tech.root: mstv
ms.assetid: 21960718-818c-4efb-a2c2-577c3b938da4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_LNBInfo interface [Microsoft TV Technologies],get_LocalOscilatorFrequencyHighBand method, IBDA_LNBInfo.get_LocalOscilatorFrequencyHighBand, IBDA_LNBInfo::get_LocalOscilatorFrequencyHighBand, IBDA_LNBInfoget_LocalOscilatorFrequencyHighBand, bdaiface/IBDA_LNBInfo::get_LocalOscilatorFrequencyHighBand, get_LocalOscilatorFrequencyHighBand, get_LocalOscilatorFrequencyHighBand method [Microsoft TV Technologies], get_LocalOscilatorFrequencyHighBand method [Microsoft TV Technologies],IBDA_LNBInfo interface, mstv.ibda_lnbinfo_get_localoscilatorfrequencyhighband
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
 - IBDA_LNBInfo.get_LocalOscilatorFrequencyHighBand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_LNBInfo::get_LocalOscilatorFrequencyHighBand


## -description



The <b>get_LocalOscilatorFrequencyHighBand</b> method retrieves the high band of the local oscillator frequency.




## -parameters




### -param pulLOFHigh [out]

Pointer that receives the high band value. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd693359(v=VS.85).aspx">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693396(v=VS.85).aspx">IBDA_LNBInfo Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693401(v=VS.85).aspx">IBDA_LNBInfo::put_LocalOscilatorFrequencyHighBand</a>
 

 

