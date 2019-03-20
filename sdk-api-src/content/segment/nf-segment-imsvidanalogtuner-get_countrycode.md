---
UID: NF:segment.IMSVidAnalogTuner.get_CountryCode
title: IMSVidAnalogTuner::get_CountryCode (segment.h)
author: windows-sdk-content
description: The get_CountryCode method retrieves the tuner's country/region code.
old-location: mstv\imsvidanalogtuner_get_countrycode.htm
tech.root: mstv
ms.assetid: f8efd47f-2a89-4982-88dd-3bfc6c00801b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_CountryCode method, IMSVidAnalogTuner.get_CountryCode, IMSVidAnalogTuner::get_CountryCode, IMSVidAnalogTunerget_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_countrycode, segment/IMSVidAnalogTuner::get_CountryCode
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidAnalogTuner.get_CountryCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidAnalogTuner::get_CountryCode


## -description


The <b>get_CountryCode</b> method retrieves the tuner's country/region code.


## -parameters




### -param lcc [out]

Pointer to a variable that receives the country/region code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Do not confuse the international country/region code with the LCID. The country/region code establishes the mapping between channel numbers and frequencies.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375950(v=VS.85).aspx">IAMTuner::get_CountryCode</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694420(v=VS.85).aspx">IMSVidAnalogTuner Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694433(v=VS.85).aspx">IMSVidAnalogTuner::put_CountryCode</a>



<a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>
 

 

