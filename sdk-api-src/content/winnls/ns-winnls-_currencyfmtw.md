---
UID: NS:winnls._currencyfmtW
title: "_currencyfmtW"
author: windows-sdk-content
description: Contains information that defines the format of a currency string. The GetCurrencyFormat function uses this information to customize a currency string for a specified locale.
old-location: intl\currencyfmt.htm
old-project: Intl
ms.assetid: 026ac9e0-1f5b-4a42-9c7b-07a127422994
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: "*LPCURRENCYFMTW, CURRENCYFMT, CURRENCYFMT structure [Internationalization for Windows Applications], CURRENCYFMTW, LPCURRENCYFMT, LPCURRENCYFMT structure pointer [Internationalization for Windows Applications], _currencyfmtW, _win32_CURRENCYFMT_str, intl.currencyfmt, winnls/CURRENCYFMT, winnls/LPCURRENCYFMT"
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
tech.root: 
req.typenames: CURRENCYFMTW, *LPCURRENCYFMTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - CURRENCYFMT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _currencyfmtW structure


## -description



Contains information that defines the format of a currency string. The <a href="https://msdn.microsoft.com/43c51deb-ca92-4e14-8c27-3b588b7be061">GetCurrencyFormat</a> function uses this information to customize a currency string for a specified locale.




## -struct-fields




### -field NumDigits

Number of fractional digits. This number is equivalent to <a href="https://msdn.microsoft.com/8c2b0bb7-296e-40cb-90a5-da131b365c1b">LOCALE_ICURRDIGITS</a>.


### -field LeadingZero

Value indicating if leading zeros should be used in decimal fields. This value is equivalent to <a href="https://msdn.microsoft.com/396d437f-09af-475f-8e73-de31d9a305da">LOCALE_ILZERO</a>.


### -field Grouping

Number of digits in each group of numbers to the left of the decimal separator specified by <b>lpDecimalSep</b>. The most significant grouping digit indicates the number of digits in the least significant group immediately to the left of the decimal separator. Each subsequent grouping digit indicates the next significant group of digits to the left of the previous group. If the last value supplied is not 0, the remaining groups repeat the last group. Typical examples of settings for this member are: 0 to group digits as in 123456789.00; 3 to group digits as in 123,456,789.00; and 32 to group digits as in 12,34,56,789.00.

<div class="alert"><b>Note</b>   You can use settings other than the typical settings, but they will not show up in the regional and language settings portion of the Control Panel. Such settings are extremely uncommon and might have unexpected results.</div>
<div> </div>

### -field lpDecimalSep

Pointer to a null-terminated decimal separator string.


### -field lpThousandSep

Pointer to a null-terminated thousand separator string.


### -field NegativeOrder

Negative currency mode. This mode is equivalent to <a href="https://msdn.microsoft.com/3a1e4a63-31bd-4ff9-a3ca-af357389e179">LOCALE_INEGCURR</a>.


### -field PositiveOrder

Positive currency mode. This mode is equivalent to <a href="https://msdn.microsoft.com/af98a851-f401-4a5a-b85f-ec9d97d7ede0">LOCALE_ICURRENCY</a>.


### -field lpCurrencySymbol

Pointer to a null-terminated currency symbol string.


## -see-also




<a href="https://msdn.microsoft.com/43c51deb-ca92-4e14-8c27-3b588b7be061">GetCurrencyFormat</a>



<a href="https://msdn.microsoft.com/75382149-7d4e-4b3e-929e-ee39bf666110">National Language Support Structures</a>
 

 

