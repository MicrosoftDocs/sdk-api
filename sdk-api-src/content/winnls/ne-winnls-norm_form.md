---
UID: NE:winnls._NORM_FORM
title: NORM_FORM (winnls.h)
description: Specifies the supported normalization forms.
helpviewer_keywords: ["NORM_FORM","NORM_FORM enumeration [Internationalization for Windows Applications]","NormalizationC","NormalizationD","NormalizationKC","NormalizationKD","NormalizationOther","_win32_NORM_FORM","intl.norm_form","winnls/NORM_FORM","winnls/NormalizationC","winnls/NormalizationD","winnls/NormalizationKC","winnls/NormalizationKD","winnls/NormalizationOther"]
old-location: intl\norm_form.htm
tech.root: Intl
ms.assetid: d0133c6d-3534-4616-8b6f-07ec712808a3
ms.date: 12/05/2018
ms.keywords: NORM_FORM, NORM_FORM enumeration [Internationalization for Windows Applications], NormalizationC, NormalizationD, NormalizationKC, NormalizationKD, NormalizationOther, _win32_NORM_FORM, intl.norm_form, winnls/NORM_FORM, winnls/NormalizationC, winnls/NormalizationD, winnls/NormalizationKC, winnls/NormalizationKD, winnls/NormalizationOther
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: NORM_FORM
req.redist: Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP
ms.custom: 19H1
f1_keywords:
 - _NORM_FORM
 - winnls/_NORM_FORM
 - NORM_FORM
 - winnls/NORM_FORM
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
 - NORM_FORM
---

# NORM_FORM enumeration


## -description

Specifies the supported normalization forms.

## -enum-fields

### -field NormalizationOther:0

Not supported.

### -field NormalizationC:0x1

Unicode normalization form C, canonical composition. Transforms each decomposed grouping, consisting of a base character plus combining characters, to the canonical precomposed equivalent. For example, A + ¨ becomes Ä.

### -field NormalizationD:0x2

Unicode normalization form D, canonical decomposition. Transforms each precomposed character to its canonical decomposed equivalent. For example, Ä becomes A + ¨.

### -field NormalizationKC:0x5

Unicode normalization form KC, compatibility composition. Transforms each base plus combining characters to the canonical precomposed equivalent and all compatibility characters to their equivalents. For example, the ligature ﬁ becomes f + i; similarly, A + ¨ + ﬁ + n becomes Ä + f + i + n.

### -field NormalizationKD:0x6      

Unicode normalization form KD, compatibility decomposition. Transforms each precomposed character to its canonical decomposed equivalent and all compatibility characters to their equivalents. For example, Ä + ﬁ + n becomes A + ¨ + f + i + n.

## -remarks

For more information about the normalization forms, see <a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-isnormalizedstring">IsNormalizedString</a>



<a href="/windows/desktop/Intl/national-language-support-enumeration-types">National Language Support Enumeration Types</a>



<a href="/windows/desktop/api/winnls/nf-winnls-normalizestring">NormalizeString</a>



<a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>
