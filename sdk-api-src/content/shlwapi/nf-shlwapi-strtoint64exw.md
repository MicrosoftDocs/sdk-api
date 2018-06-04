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

# StrToInt64ExW function


## -description


Converts a string representing a decimal or hexadecimal value to a 64-bit integer.


## -parameters




### -param pszString [in]

Type: <b>PCTSTR</b>

A pointer to the <b>null</b>-terminated string to be converted. For further details concerning the valid forms of the string, see the Remarks section.


### -param dwFlags

Type: <b>STIF_FLAGS</b>

One of the following values that specify how <i>pszString</i> should be parsed for its conversion to a 64-bit integer.



#### STIF_DEFAULT

The string at <i>pszString</i> contains the representation of a decimal value.



#### STIF_SUPPORT_HEX

The string at <i>pszString</i> contains the representation of either a decimal or hexadecimal value. Note that in hexadecimal representations, the characters A-F are case-insensitive.


### -param pllRet [out]

Type: <b>LONGLONG*</b>

A pointer to a variable of type <b>LONGLONG</b> that receives the 64-bit integer value of the converted string. For instance, in the case of the string "123", the integer pointed to by this value receives the value 123. 

                    

If this function returns <b>FALSE</b>, this value is undefined.

If the value returned is too large to be contained in a variable of type <b>LONGLONG</b>, this parameter contains the 64 low-order bits of the value. Any high-order bits beyond that are lost.


##### - dwFlags.STIF_DEFAULT

The string at <i>pszString</i> contains the representation of a decimal value.


##### - dwFlags.STIF_SUPPORT_HEX

The string at <i>pszString</i> contains the representation of either a decimal or hexadecimal value. Note that in hexadecimal representations, the characters A-F are case-insensitive.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string is converted; otherwise <b>FALSE</b>.




## -remarks



The string pointed to by the <i>pszString</i> parameter must have one of the following forms to be parsed successfully.

                

<ul>
<li>This form is accepted as a decimal value under either flag.
                        <pre class="syntax" xml:space="preserve"><code>(optional white space)(optional sign)(one or more decimal digits)</code></pre>
</li>
<li>These forms are required for hexadecimal values when the STIF_SUPPORT_HEX flag is passed.
                        <pre class="syntax" xml:space="preserve"><code>(optional white space)(optional sign)0x(one or more hexadecimal digits)</code></pre>
<pre class="syntax" xml:space="preserve"><code>(optional white space)(optional sign)0X(one or more hexadecimal digits)</code></pre>
</li>
</ul>
The optional sign can be the character '-' or '+'; if omitted, the sign is assumed to be positive.

<div class="alert"><b>Note</b>  If the value is parsed as hexadecimal, the optional sign is ignored, even if it is a '-' character. For example, the string "-0x1" is parsed as 1 instead of -1.</div>
<div> </div>
If the string pointed to by <i>pszString</i> contains an invalid character, that character is considered the end of the string to be converted and the remainder is ignored. For instance, given the invalid hexadecimal string "0x00am123", <b>StrToInt64Ex</b> only recognizes "0x00a", converts it to the integer value 10, and returns <b>TRUE</b>.

If <i>pllRet</i> is <b>NULL</b>, the function returns <b>TRUE</b> if the string can be converted, even though it does not perform the conversion.



