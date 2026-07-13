---
UID: NF:winnls.IS_HIGH_SURROGATE
title: IS_HIGH_SURROGATE macro (winnls.h)
description: Determines if a character is a UTF-16 high surrogate code point, ranging from 0xd800 to 0xdbff, inclusive.
helpviewer_keywords: ["IS_HIGH_SURROGATE","IS_HIGH_SURROGATE macro [Internationalization for Windows Applications]","_win32_IS_HIGH_SURROGATE","intl.is_high_surrogate","winnls/IS_HIGH_SURROGATE"]
old-location: intl\is_high_surrogate.htm
tech.root: Intl
ms.assetid: d491dfd9-e0f4-47cf-96ef-83dc22a1af81
ms.date: 07/01/2025
ms.keywords: IS_HIGH_SURROGATE, IS_HIGH_SURROGATE macro [Internationalization for Windows Applications], _win32_IS_HIGH_SURROGATE, intl.is_high_surrogate, winnls/IS_HIGH_SURROGATE
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IS_HIGH_SURROGATE
 - winnls/IS_HIGH_SURROGATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - IS_HIGH_SURROGATE
---

# IS_HIGH_SURROGATE macro

## -syntax

```cpp
bool IS_HIGH_SURROGATE(
    WCHAR wch
);
```

## -returns

Type: **bool**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

Determines if a character is a UTF-16 high <a href="/windows/desktop/Intl/surrogates-and-supplementary-characters">surrogate</a> code point, ranging from 0xd800 to 0xdbff, inclusive.

## -parameters

### -param wch

Character to test.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-is_low_surrogate">IS_LOW_SURROGATE</a>



<a href="/windows/desktop/api/winnls/nf-winnls-is_surrogate_pair">IS_SURROGATE_PAIR</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="/windows/desktop/Intl/surrogates-and-supplementary-characters">Surrogates and Supplementary Characters</a>
