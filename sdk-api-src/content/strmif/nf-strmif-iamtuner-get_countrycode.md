---
UID: NF:strmif.IAMTuner.get_CountryCode
title: IAMTuner::get_CountryCode
author: windows-sdk-content
description: The get_CountryCode method retrieves the country/region code that establishes the current channel-to-frequency mapping.
old-location: dshow\iamtuner_get_countrycode.htm
tech.root: DirectShow
ms.assetid: 8b459ad8-c9e0-4b35-aec4-113c8a67d907
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAMTuner interface [DirectShow],get_CountryCode method, IAMTuner.get_CountryCode, IAMTuner::get_CountryCode, IAMTunerget_CountryCode, dshow.iamtuner_get_countrycode, get_CountryCode, get_CountryCode method [DirectShow], get_CountryCode method [DirectShow],IAMTuner interface, strmif/IAMTuner::get_CountryCode
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner.get_CountryCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTuner::get_CountryCode


## -description



The <code>get_CountryCode</code> method retrieves the country/region code that establishes the current channel-to-frequency mapping.




## -parameters




### -param plCountryCode [out]

Pointer to a variable that receives the country/region code currently in use by the <a href="https://msdn.microsoft.com/a8e101dc-78ab-495f-9086-7b1d1e87c357">TV Tuner</a> filter.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



The <a href="https://msdn.microsoft.com/d733f829-5600-4f75-9bc9-de8dc8dd8031">IAMTuner::put_CountryCode</a> method determines which channel-to-frequency mapping table to use. This establishes the base frequencies for the given country/region. Use the <a href="https://msdn.microsoft.com/ae8338e4-b75d-42d5-bcb7-84352921458c">IAMTVTuner::AutoTune</a> method to determine the exact frequencies for specific regions.

Override the country/region code when a country/region wants to receive broadcast video from a different national source. For a list of country/region codes, see <a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

