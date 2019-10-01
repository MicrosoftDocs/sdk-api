---
UID: NF:winnls.IS_SURROGATE_PAIR
title: IS_SURROGATE_PAIR macro (winnls.h)
author: windows-sdk-content
description: Determines if the specified code units form a UTF-16 surrogate pair.
old-location: intl\is_surrogate_pair.htm
tech.root: Intl
ms.assetid: cf7bf905-2cf7-416f-985f-cda4e03b86f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IS_SURROGATE_PAIR, IS_SURROGATE_PAIR macro [Internationalization for Windows Applications], _win32_IS_SURROGATE_PAIR, intl.is_surrogate_pair, winnls/IS_SURROGATE_PAIR
ms.topic: macro
f1_keywords: 
 - "winnls/IS_SURROGATE_PAIR"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - IS_SURROGATE_PAIR
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IS_SURROGATE_PAIR macro


## -description


Determines if the specified code units form a UTF-16 <a href="https://docs.microsoft.com/windows/desktop/Intl/surrogates-and-supplementary-characters">surrogate pair</a>.


## -parameters




### -param hs

UTF-16 code unit to test for a high surrogate value. The range for a high UTF-16 code unit is 0xd800 to 0xdbff, inclusive.


### -param ls

UTF-16 code unit to test for a low surrogate value. The range for a low UTF-16 code unit is 0xdc00 to 0xdfff, inclusive.


## -remarks



For this macro to succeed, the <i>hs</i> value must be a high UTF-16 code unit, and the <i>ls</i> value must be a low UTF-16 code unit.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-is_high_surrogate">IS_HIGH_SURROGATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-is_low_surrogate">IS_LOW_SURROGATE</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/surrogates-and-supplementary-characters">Surrogates and Supplementary Characters</a>
 

 

