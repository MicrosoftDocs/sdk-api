---
UID: NF:bdaiface.IBDA_FrequencyFilter.put_Range
title: IBDA_FrequencyFilter::put_Range
author: windows-sdk-content
description: The put_Range method specifies the tuner range. The tuner range is the frequency domain on which to find a particular carrier frequency.
old-location: mstv\ibda_frequencyfilter_put_range.htm
old-project: mstv
ms.assetid: 3567c723-13ef-4306-81dd-2e844abeeb04
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_FrequencyFilter interface [Microsoft TV Technologies],put_Range method, IBDA_FrequencyFilter.put_Range, IBDA_FrequencyFilter::put_Range, IBDA_FrequencyFilterput_Range, bdaiface/IBDA_FrequencyFilter::put_Range, mstv.ibda_frequencyfilter_put_range, put_Range, put_Range method [Microsoft TV Technologies], put_Range method [Microsoft TV Technologies],IBDA_FrequencyFilter interface
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
 - IBDA_FrequencyFilter.put_Range
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_FrequencyFilter::put_Range


## -description



The <b>put_Range</b> method specifies the tuner range. The <i>tuner range</i> is the frequency domain on which to find a particular carrier frequency




## -parameters




### -param ulRange [in]

Specifies the tuner range. The units are 1 Hz x the frequency multiplier, where the <i>frequency multiplier</i> is the value returned by the <a href="https://msdn.microsoft.com/463a58f7-a10c-40b5-8183-3e16bcc7c6b2">IBDA_FrequencyFilter::get_FrequencyMultiplier</a> method. The default frequency multiplier is 1000, so the default units are kilohertz (kHz). If you set this parameter value to -1, the tuner range is not set. If you set the parameter value to 0, the tuner range is undefined.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ef5dbf4a-ecbb-4f2c-a34d-ce3864133adc">IBDA_FrequencyFilter Interface</a>



<a href="https://msdn.microsoft.com/463a58f7-a10c-40b5-8183-3e16bcc7c6b2">IBDA_FrequencyFilter::get_FrequencyMultiplier</a>



<a href="https://msdn.microsoft.com/fdf96400-8fd9-4989-9977-026a9bec37ea">IBDA_FrequencyFilter::get_Range</a>
 

 

