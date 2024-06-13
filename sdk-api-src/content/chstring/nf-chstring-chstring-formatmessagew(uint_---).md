---
UID: NF:chstring.CHString.FormatMessageW(UINT,...)
title: CHString::FormatMessageW(UINT,...)
description: The CHString::FormatMessageW (Unicode) method formats a message string.
tech.root: wmi
helpviewer_keywords: ["CHString::FormatMessageW"]
ms.assetid: efa2f907-3a83-4508-95ef-5d40513f507e
ms.date: 08/10/2022
ms.keywords: CHString::FormatMessageW
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: chstring.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - CHString::FormatMessageW
 - chstring/CHString::FormatMessageW
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - chstring.h
api_name:
 - CHString::FormatMessageW
---

## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new development.]

The **FormatMessageW** method formats a message string.

## -parameters

### -param nFormatID

The string resource identifier that contains the unformatted message text.

### -param ...

Argument list.

## -returns

CHeap_Exception

## -remarks

The **FormatMessageW** method requires a message definition as input.
The message definition is determined by *lpszFormat* or from the string resource identified by *nFormatID*.
The method copies the formatted message text to the **CHString** string, processing any embedded insert sequences if requested.

Each insert must have a corresponding parameter that follows the *lpszFormat* or *nFormatID* parameter.
Within the message text, several escape sequences are supported for dynamically formatting the message.
For a description of these escape sequences and their meanings, see the Windows **FormatMessage** function topic.

**Note** To reduce exposure to security attacks, always use a format string for **FormatMessageW**.
For example, **FormatMessageW(input)** is exploitable, and **FormatMessageW("%s", input)** is not.
Never use a user-supplied string for the format string.
If your format string is stored for a purpose such as localization, ensure that the string is protected from unauthorized write access.
If your function writes to a string rather than standard output, you may need to avoid using a trailing "%s" in the format string.

## Examples

The following code example shows you how to use **CHString::FormatMessageW**.

```cpp
CHString str;
int nAsked = 5;
int nAgree = 4;

str.FormatMessageW(L"%1!d! of %2!d! developers agree: Golf is %3%!", 
   nAgree, nAsked, L"Best");
assert(str == L"4 of 5 developers agree: Golf is Best!");
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>

<a href="/windows/desktop/api/chstring/nf-chstring-chstring-format(uint_---)">CHString::Format</a>
