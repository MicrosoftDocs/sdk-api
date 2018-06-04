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

# _currencyfmtA structure


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
 

 

