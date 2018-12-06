---
UID: NF:segment.IMSVidAnalogTuner.get_CountryCode
title: IMSVidAnalogTuner::get_CountryCode
author: windows-sdk-content
description: The get_CountryCode method retrieves the tuner's country/region code.
old-location: mstv\imsvidanalogtuner_get_countrycode.htm
tech.root: mstv
ms.assetid: f8efd47f-2a89-4982-88dd-3bfc6c00801b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_CountryCode method, IMSVidAnalogTuner.get_CountryCode, IMSVidAnalogTuner::get_CountryCode, IMSVidAnalogTunerget_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_countrycode, segment/IMSVidAnalogTuner::get_CountryCode
ms.prod: windows-hardware
ms.technology: windows-devices
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




<a href="https://msdn.microsoft.com/8b459ad8-c9e0-4b35-aec4-113c8a67d907">IAMTuner::get_CountryCode</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>



<a href="https://msdn.microsoft.com/e6ec6975-8953-45df-9d86-cf8b8888bba6">IMSVidAnalogTuner::put_CountryCode</a>



<a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>
 

 

