---
UID: NF:tuner.IAnalogTVTuningSpace.put_CountryCode
title: IAnalogTVTuningSpace::put_CountryCode
author: windows-sdk-content
description: The put_CountryCode method sets the country/region code of the tuning space (based on TAPI country/region codes).
old-location: mstv\ianalogtvtuningspace_put_countrycode.htm
old-project: mstv
ms.assetid: eb53bdfe-6293-41f3-8945-5f960193df9e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],put_CountryCode method, IAnalogTVTuningSpace.put_CountryCode, IAnalogTVTuningSpace::put_CountryCode, IAnalogTVTuningSpaceput_CountryCode, mstv.ianalogtvtuningspace_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, tuner/IAnalogTVTuningSpace::put_CountryCode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IAnalogTVTuningSpace.put_CountryCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogTVTuningSpace::put_CountryCode


## -description



The <b>put_CountryCode</b> method sets the country/region code of the tuning space (based on TAPI country/region codes).




## -parameters




### -param NewCountryCodeVal [in]

The country/region code.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The tuner can use the country/region code to locate a likely channel for frequency mapping.




## -see-also




<a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace Interface</a>
 

 

