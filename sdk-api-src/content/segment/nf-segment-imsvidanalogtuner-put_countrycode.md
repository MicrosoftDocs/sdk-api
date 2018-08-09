---
UID: NF:segment.IMSVidAnalogTuner.put_CountryCode
title: IMSVidAnalogTuner::put_CountryCode
author: windows-sdk-content
description: The put_CountryCode method specifies the tuner's country/region code.
old-location: mstv\imsvidanalogtuner_put_countrycode.htm
old-project: mstv
ms.assetid: e6ec6975-8953-45df-9d86-cf8b8888bba6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],put_CountryCode method, IMSVidAnalogTuner.put_CountryCode, IMSVidAnalogTuner::put_CountryCode, IMSVidAnalogTunerput_CountryCode, mstv.imsvidanalogtuner_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IMSVidAnalogTuner interface, segment/IMSVidAnalogTuner::put_CountryCode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAnalogTuner.put_CountryCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidAnalogTuner::put_CountryCode


## -description


The <b>put_CountryCode</b> method specifies the tuner's country/region code.


## -parameters




### -param lcc [in]

Specifies the international country/region code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Do not confuse the international country/region code with the LCID. The country/region code establishes the mapping between channel numbers and frequencies.




## -see-also




<a href="https://msdn.microsoft.com/d733f829-5600-4f75-9bc9-de8dc8dd8031">IAMTuner::put_CountryCode</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>



<a href="https://msdn.microsoft.com/f8efd47f-2a89-4982-88dd-3bfc6c00801b">IMSVidAnalogTuner::get_CountryCode</a>



<a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>
 

 

