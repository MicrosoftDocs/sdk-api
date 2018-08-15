---
UID: NF:tuner.IAuxInTuningSpace2.get_CountryCode
title: IAuxInTuningSpace2::get_CountryCode
author: windows-sdk-content
description: This topic applies to Windows XP Media Center Edition 2004 and later.
old-location: mstv\iauxintuningspace2_get_countrycode.htm
old-project: mstv
ms.assetid: dffd3ad2-2caa-4041-9e24-024050414a87
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAuxInTuningSpace2 interface [Microsoft TV Technologies],get_CountryCode method, IAuxInTuningSpace2.get_CountryCode, IAuxInTuningSpace2::get_CountryCode, IAuxInTuningSpace2get_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IAuxInTuningSpace2 interface, mstv.iauxintuningspace2_get_countrycode, tuner/IAuxInTuningSpace2::get_CountryCode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
 - IAuxInTuningSpace2.get_CountryCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAuxInTuningSpace2::get_CountryCode


## -description



This topic applies to Windows XP Media Center Edition 2004 and later.
        



The <b>get_CountryCode</b> method gets the country/region code of the tuning space (based on TAPI country/region codes).


## -parameters




### -param CountryCodeVal [out]

Pointer to a variable that receives the country/region code.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51d92eab-1cf0-451c-aefb-ca36360e29f7">IAuxInTuningSpace2 Interface</a>
 

 

