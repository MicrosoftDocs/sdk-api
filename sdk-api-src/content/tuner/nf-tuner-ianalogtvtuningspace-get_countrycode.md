---
UID: NF:tuner.IAnalogTVTuningSpace.get_CountryCode
title: IAnalogTVTuningSpace::get_CountryCode
author: windows-sdk-content
description: The get_CountryCode method gets the country/region code of the tuning space (based on TAPI country/region codes).
old-location: mstv\ianalogtvtuningspace_get_countrycode.htm
tech.root: mstv
ms.assetid: f74f31cc-8e3a-41b8-bf27-f60b9cbcfcdb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],get_CountryCode method, IAnalogTVTuningSpace.get_CountryCode, IAnalogTVTuningSpace::get_CountryCode, IAnalogTVTuningSpaceget_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, mstv.ianalogtvtuningspace_get_countrycode, tuner/IAnalogTVTuningSpace::get_CountryCode
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IAnalogTVTuningSpace.get_CountryCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAnalogTVTuningSpace::get_CountryCode


## -description



The <b>get_CountryCode</b> method gets the country/region code of the tuning space (based on TAPI country/region codes).




## -parameters




### -param CountryCodeVal [out]

Receives the value for the country/region code.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The tuner can use the country/region code to locate a likely channel for frequency mapping.




## -see-also




<a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace Interface</a>
 

 

