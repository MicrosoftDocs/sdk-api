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

# VarParseNumFromStr function


## -description


Parses a string, and creates a type-independent description of the number it represents.


## -parameters




### -param strIn [in]

The input string to convert.


### -param lcid [in]

The locale identifier.


### -param dwFlags [in]

Enables the caller to control parsing, therefore defining the acceptable syntax of a number. If this field is set to zero, the input string must contain nothing but decimal digits. Setting each defined flag bit enables parsing of that syntactic feature. Standard Automation parsing (for example, as used by <a href="https://msdn.microsoft.com/a4f43356-5681-4926-aa2a-471fa2198a2c">VarI2FromStr</a>) has all flags set (NUMPRS_STD).



### -param pnumprs [out]

The parsed results.


### -param rgbDig [out]

The values for the digits in the range 0–7, 0–9, or 0–15, depending on whether the number is octal, decimal, or hexadecimal. All leading zeros have been stripped off. For decimal numbers, trailing zeros are also stripped off, unless the number is zero, in which case a single zero digit will be present.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Internal memory allocation failed. (Used for DBCS only to create a copy with all wide characters mapped narrow.)


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
There is no valid number in the string, or there is no closing parenthesis to match an opening one. In the former case, cDig and cchUsed in the NUMPARSE structure will be zero. In the latter, the NUMPARSE structure and digit array are fully updated, as if the closing parenthesis was present.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
For hexadecimal and octal digits, there are more digits than will fit into the array. For decimal, the exponent exceeds the maximum possible. In both cases, the NUMPARSE structure and digit array are fully updated (for decimal, the cchUsed field excludes the entire exponent).


</td>
</tr>
</table>
 



