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

# IS_SURROGATE_PAIR macro


## -description


Determines if the specified code units form a UTF-16 <a href="https://msdn.microsoft.com/0dea39e2-a2b4-47fc-b44a-56af8ba1e346">surrogate pair</a>.


## -parameters




### -param hs

UTF-16 code unit to test for a high surrogate value. The range for a high UTF-16 code unit is 0xd800 to 0xdbff, inclusive.


### -param ls

UTF-16 code unit to test for a low surrogate value. The range for a low UTF-16 code unit is 0xdc00 to 0xdfff, inclusive.


## -remarks



For this macro to succeed, the <i>hs</i> value must be a high UTF-16 code unit, and the <i>ls</i> value must be a low UTF-16 code unit.




## -see-also




<a href="https://msdn.microsoft.com/d491dfd9-e0f4-47cf-96ef-83dc22a1af81">IS_HIGH_SURROGATE</a>



<a href="https://msdn.microsoft.com/5f60b88b-4e3d-4e0a-803d-ab407425d92a">IS_LOW_SURROGATE</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>



<a href="https://msdn.microsoft.com/0dea39e2-a2b4-47fc-b44a-56af8ba1e346">Surrogates and Supplementary Characters</a>
 

 

