---
UID: NF:bdaiface.IBDA_FrequencyFilter.get_Range
title: IBDA_FrequencyFilter::get_Range
author: windows-sdk-content
description: The get_Range method retrieves the tuner range. The tuner range is the frequency domain on which to find a particular carrier frequency.
old-location: mstv\ibda_frequencyfilter_get_range.htm
tech.root: mstv
ms.assetid: fdf96400-8fd9-4989-9977-026a9bec37ea
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],get_Range method, IBDA_FrequencyFilter.get_Range, IBDA_FrequencyFilter::get_Range, IBDA_FrequencyFilterget_Range, bdaiface/IBDA_FrequencyFilter::get_Range, get_Range, get_Range method [Microsoft TV Technologies], get_Range method [Microsoft TV Technologies],IBDA_FrequencyFilter interface, mstv.ibda_frequencyfilter_get_range
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
 - IBDA_FrequencyFilter.get_Range
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_FrequencyFilter::get_Range


## -description



The get_Range method retrieves the tuner range. The <i>tuner range</i> is the frequency domain on which to find a particular carrier frequency




## -parameters




### -param pulRange [out]

Pointer that receives the tuner range. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd693359(v=VS.85).aspx">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz). A value of -1 for this parameter indicates that the tuner range is not set. A value of 0 for this parameter indicates that  the tuner range is undefined.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693355(v=VS.85).aspx">IBDA_FrequencyFilter Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693359(v=VS.85).aspx">IBDA_FrequencyFilter::get_FrequencyMultiplier</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693367(v=VS.85).aspx">IBDA_FrequencyFilter::put_Range</a>
 

 

