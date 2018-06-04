---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

