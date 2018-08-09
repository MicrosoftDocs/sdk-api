---
UID: NF:winnls.IS_SURROGATE_PAIR
title: IS_SURROGATE_PAIR macro
author: windows-sdk-content
description: Determines if the specified code units form a UTF-16 surrogate pair.
old-location: intl\is_surrogate_pair.htm
old-project: Intl
ms.assetid: cf7bf905-2cf7-416f-985f-cda4e03b86f9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IS_SURROGATE_PAIR, IS_SURROGATE_PAIR macro [Internationalization for Windows Applications], _win32_IS_SURROGATE_PAIR, intl.is_surrogate_pair, winnls/IS_SURROGATE_PAIR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winnls.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - IS_SURROGATE_PAIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

