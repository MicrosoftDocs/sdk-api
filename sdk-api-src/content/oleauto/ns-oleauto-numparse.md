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

# NUMPARSE structure


## -description


Specifies numeric parsing information.


## -struct-fields




### -field cDig

On input, the size of the array. On output, the number of items written to the rgbDig array.


### -field dwInFlags

Input flags.



#### NUMPRS_CURRENCY (0x0400)



#### NUMPRS_DECIMAL (0x0100)



#### NUMPRS_EXPONENT (0x0800)



#### NUMPRS_HEX_OCT (0x0040)



#### NUMPRS_LEADING_MINUS (0x0100)



#### NUMPRS_LEADING_PLUS (0x0004)



#### NUMPRS_LEADING_WHITE (0x0001)



#### NUMPRS_PARENS (0x0080)



#### NUMPRS_STD (0x1FFF)



#### NUMPRS_THOUSANDS (0x0200)



#### NUMPRS_TRAILING_MINUS (0x0020)



#### NUMPRS_TRAILING_PLUS (0x0008)



#### NUMPRS_TRAILING_WHITE (0x0002)



#### NUMPRS_USE_ALL (0x1000)


### -field dwOutFlags

Output flags. Includes all the values for <b>dwInFlags</b>, plus the following values.



#### NUMPRS_INEXACT (0x20000)



#### NUMPRS_NEG (0x10000)


### -field cchUsed

Receives the number of characters (from the beginning of the string) that were successfully parsed.


### -field nBaseShift

The number of bits per digit (3 or 4 for octal and hexadecimal numbers, and zero for decimal).



### -field nPwr10

The decimal point position.


## -remarks



The following apply only to decimal numbers:

<ul>
<li><b>nPwr10</b> sets the decimal point position by giving the power of 10 of the least significant digit.</li>
<li>If the number is negative, <b>NUMPRS_NEG</b> will be set in <b>dwOutFlags</b>.</li>
<li>If there are more non-zero decimal digits than will fit into the digit array, the NUMPRS_INEXACT flag will be set.
</li>
</ul>


