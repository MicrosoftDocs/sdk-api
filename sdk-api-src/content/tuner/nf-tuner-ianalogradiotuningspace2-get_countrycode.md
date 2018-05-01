---
UID: NF:tuner.IAnalogRadioTuningSpace2.get_CountryCode
title: IAnalogRadioTuningSpace2::get_CountryCode method
author: windows-driver-content
description: This topic applies to Windows XP Media Center Edition 2004 and later.
old-location: mstv\ianalogradiotuningspace2_get_countrycode.htm
old-project: mstv
ms.assetid: dc619247-90fc-4db0-9b46-cc81b9ae6916
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAnalogRadioTuningSpace2, IAnalogRadioTuningSpace2 interface [Microsoft TV Technologies], get_CountryCode method, IAnalogRadioTuningSpace2::get_CountryCode, IAnalogRadioTuningSpace2get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies], IAnalogRadioTuningSpace2 interface, get_CountryCode,IAnalogRadioTuningSpace2.get_CountryCode, mstv.ianalogradiotuningspace2_get_countrycode, tuner/IAnalogRadioTuningSpace2::get_CountryCode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IAnalogRadioTuningSpace2.get_CountryCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogRadioTuningSpace2::get_CountryCode method


## -description



This topic applies to Windows XP Media Center Edition 2004 and later.
        



The <b>get_CountryCode</b> method gets the country/region code of the tuning space (based on TAPI country/region codes).


## -parameters




### -param CountryCodeVal [out]

Pointer to a variable that receives the country/region code.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/66e631cb-2ae8-40b0-8ec8-3a02764284bf">IAnalogRadioTuningSpace2 Interface</a>
 

 

