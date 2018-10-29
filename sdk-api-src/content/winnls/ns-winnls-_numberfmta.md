---
UID: NS:winnls._numberfmtA
title: "_numberfmtA"
author: windows-sdk-content
description: Contains information that defines the format of a number string. The GetNumberFormat function uses this information to customize a number string for a specified locale.
old-location: intl\numberfmt.htm
tech.root: Intl
ms.assetid: cb8a7714-3777-41b4-894b-bb0c0797d51e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPNUMBERFMTA, LPNUMBERFMT, LPNUMBERFMT structure pointer [Internationalization for Windows Applications], NUMBERFMT, NUMBERFMT structure [Internationalization for Windows Applications], NUMBERFMTA, _numberfmtA, _win32_NUMBERFMT_str, intl.numberfmt, winnls/LPNUMBERFMT, winnls/NUMBERFMT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - NUMBERFMT
product: Windows
targetos: Windows
req.typenames: NUMBERFMTA, *LPNUMBERFMTA
req.redist: 
---

# _numberfmtA structure


## -description



Contains information that defines the format of a number string. The <a href="https://msdn.microsoft.com/acbfebed-71bd-4266-b639-66f453158442">GetNumberFormat</a> function uses this information to customize a number string for a specified locale.




## -struct-fields




### -field NumDigits

Number of fractional digits. This value is equivalent to the locale information specified by the value <a href="https://msdn.microsoft.com/ecd014c9-76c5-44a3-8fbd-5b7dc34834f9">LOCALE_IDIGITS</a>.


### -field LeadingZero

A value indicating if leading zeros should be used in decimal fields. This value is equivalent to the locale information specified by the value <a href="https://msdn.microsoft.com/396d437f-09af-475f-8e73-de31d9a305da">LOCALE_ILZERO</a>.


### -field Grouping

Number of digits in each group of numbers to the left of the decimal separator specified by <b>lpDecimalSep</b>. Values in the range 0 through 9 and 32 are valid. The most significant grouping digit indicates the number of digits in the least significant group immediately to the left of the decimal separator. Each subsequent grouping digit indicates the next significant group of digits to the left of the previous group. If the last value supplied is not 0, the remaining groups repeat the last group. Typical examples of settings for this member are: 0 to group digits as in 123456789.00; 3 to group digits as in 123,456,789.00; and 32 to group digits as in 12,34,56,789.00.

<div class="alert"><b>Note</b>   You can use settings other than the typical settings, but they will not show up in the regional and language options portion of the Control Panel. Such settings are extremely uncommon and might have unexpected results.</div>
<div> </div>

### -field lpDecimalSep

Pointer to a null-terminated decimal separator string.


### -field lpThousandSep

Pointer to a null-terminated thousand separator string.


### -field NegativeOrder

Negative number mode. This mode is equivalent to the locale information specified by the value <a href="https://msdn.microsoft.com/3a1e4a63-31bd-4ff9-a3ca-af357389e179">LOCALE_INEGNUMBER</a>.


## -see-also




<a href="https://msdn.microsoft.com/acbfebed-71bd-4266-b639-66f453158442">GetNumberFormat</a>



<a href="https://msdn.microsoft.com/75382149-7d4e-4b3e-929e-ee39bf666110">National Language Support Structures</a>
 

 

