---
UID: NS:winnls._numberfmtW
title: NUMBERFMTW (winnls.h)
description: Contains information that defines the format of a number string. The GetNumberFormat function uses this information to customize a number string for a specified locale. (Unicode)
helpviewer_keywords: ["*LPNUMBERFMTW","LPNUMBERFMT","LPNUMBERFMT structure pointer [Internationalization for Windows Applications]","NUMBERFMT","NUMBERFMT structure [Internationalization for Windows Applications]","NUMBERFMTW","_win32_NUMBERFMT_str","intl.numberfmt","winnls/LPNUMBERFMT","winnls/NUMBERFMT"]
old-location: intl\numberfmt.htm
tech.root: Intl
ms.assetid: cb8a7714-3777-41b4-894b-bb0c0797d51e
ms.date: 12/05/2018
ms.keywords: '*LPNUMBERFMTW, LPNUMBERFMT, LPNUMBERFMT structure pointer [Internationalization for Windows Applications], NUMBERFMT, NUMBERFMT structure [Internationalization for Windows Applications], NUMBERFMTW, _win32_NUMBERFMT_str, intl.numberfmt, winnls/LPNUMBERFMT, winnls/NUMBERFMT'
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: NUMBERFMTW, *LPNUMBERFMTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _numberfmtW
 - winnls/_numberfmtW
 - LPNUMBERFMTW
 - winnls/LPNUMBERFMTW
 - NUMBERFMTW
 - winnls/NUMBERFMTW
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
 - NUMBERFMT
---

# NUMBERFMTW structure


## -description

Contains information that defines the format of a number string. The <a href="/windows/desktop/api/winnls/nf-winnls-getnumberformata">GetNumberFormat</a> function uses this information to customize a number string for a specified locale.

## -struct-fields

### -field NumDigits

Number of fractional digits. This value is equivalent to the locale information specified by the value <a href="/windows/desktop/Intl/locale-idigits">LOCALE_IDIGITS</a>.

### -field LeadingZero

A value indicating if leading zeros should be used in decimal fields. This value is equivalent to the locale information specified by the value <a href="/windows/desktop/Intl/locale-ilzero">LOCALE_ILZERO</a>.

### -field Grouping

Number of digits in each group of numbers to the left of the decimal separator specified by <b>lpDecimalSep</b>. Values in the range 0 through 9 and 32 are valid. The most significant grouping digit indicates the number of digits in the least significant group immediately to the left of the decimal separator. Each subsequent grouping digit indicates the next significant group of digits to the left of the previous group. If the last value supplied is not 0, the remaining groups repeat the last group. Typical examples of settings for this member are: 0 to group digits as in 123456789.00; 3 to group digits as in 123,456,789.00; and 32 to group digits as in 12,34,56,789.00.

<div class="alert"><b>Note</b>   You can use settings other than the typical settings, but they will not show up in the regional and language options portion of the Control Panel. Such settings are extremely uncommon and might have unexpected results.</div>
<div> </div>

### -field lpDecimalSep

Pointer to a null-terminated decimal separator string.

### -field lpThousandSep

Pointer to a null-terminated thousand separator string.

### -field NegativeOrder

Negative number mode. This mode is equivalent to the locale information specified by the value <a href="/windows/desktop/Intl/locale-ineg-constants">LOCALE_INEGNUMBER</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getnumberformata">GetNumberFormat</a>



<a href="/windows/desktop/Intl/national-language-support-structures">National Language Support Structures</a>

## -remarks

> [!NOTE]
> The winnls.h header defines NUMBERFMT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
