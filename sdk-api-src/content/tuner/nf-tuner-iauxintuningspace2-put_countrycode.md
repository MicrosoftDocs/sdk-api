---
UID: NF:tuner.IAuxInTuningSpace2.put_CountryCode
title: IAuxInTuningSpace2::put_CountryCode
author: windows-sdk-content
description: This topic applies to Windows XP Media Center Edition 2004 and later.
old-location: mstv\iauxintuningspace2_put_countrycode.htm
old-project: mstv
ms.assetid: 4c589a79-c71f-40fc-8bf2-5163ae652d70
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAuxInTuningSpace2 interface [Microsoft TV Technologies],put_CountryCode method, IAuxInTuningSpace2.put_CountryCode, IAuxInTuningSpace2::put_CountryCode, IAuxInTuningSpace2put_CountryCode, mstv.iauxintuningspace2_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IAuxInTuningSpace2 interface, tuner/IAuxInTuningSpace2::put_CountryCode
ms.prod: windows
ms.technology: windows-sdk
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
 - IAuxInTuningSpace2.put_CountryCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAuxInTuningSpace2::put_CountryCode


## -description



This topic applies to Windows XP Media Center Edition 2004 and later.
        



The <b>put_CountryCode</b> method sets the country/region code of the tuning space (based on TAPI country/region codes).


## -parameters




### -param NewCountryCodeVal [in]

The country/region code.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51d92eab-1cf0-451c-aefb-ca36360e29f7">IAuxInTuningSpace2 Interface</a>
 

 

