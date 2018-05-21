---
UID: NF:strmif.IAMTuner.put_CountryCode
title: IAMTuner::put_CountryCode
author: windows-driver-content
description: The put_CountryCode method sets the country/region code to establish the frequency to use.
old-location: dshow\iamtuner_put_countrycode.htm
old-project: DirectShow
ms.assetid: d733f829-5600-4f75-9bc9-de8dc8dd8031
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMTuner interface [DirectShow],put_CountryCode method, IAMTuner.put_CountryCode, IAMTuner::put_CountryCode, IAMTunerput_CountryCode, dshow.iamtuner_put_countrycode, put_CountryCode, put_CountryCode method [DirectShow], put_CountryCode method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_CountryCode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTuner.put_CountryCode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTuner::put_CountryCode


## -description



The <code>put_CountryCode</code> method sets the country/region code to establish the frequency to use.




## -parameters




### -param lCountryCode [in]

Value indicating the country/region code.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method establishes the base frequencies for the given country/region. Use the <a href="https://msdn.microsoft.com/ae8338e4-b75d-42d5-bcb7-84352921458c">IAMTVTuner::AutoTune</a> method to determine the exact frequencies for specific regions, unless there are previously cached settings for the new country/region.

Because channels in different countries/regions map to different frequencies, worldwide mapping tables are provided in the appendix <a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>. Override the existing country/region code by selecting the new value from the appendix and passing it in as the parameter for the <code>put_CountryCode</code> method. This is useful when a country/region wants to receive broadcast video from a different national source.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

