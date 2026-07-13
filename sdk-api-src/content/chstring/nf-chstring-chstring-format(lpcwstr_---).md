---
UID: NF:chstring.CHString.Format(LPCWSTR,...)
title: CHString::Format(LPCWSTR,...)
description: The CHString::Format method formats and stores a series of characters and values in a CHString.
tech.root: wmi
helpviewer_keywords: ["CHString::Format"]
ms.assetid: 2187385b-8e30-4620-be1a-8c95c4d870b1
ms.date: 08/10/2022
ms.keywords: CHString::Format
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
 - CHString::Format
 - chstring/CHString::Format
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - chstring.h
api_name:
 - CHString::Format
---

## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new development.]

The **Format** method formats and stores a series of characters and values in a **CHString**.

## -parameters

### -param lpszFormat

Format-control string.

### -param ...

Argument list.

## -returns

CHeap_Exception

## -remarks

Each optional argument (if any) is converted and output according to the corresponding format specification in *lpszFormat*, or from the string resource identified by *nFormatID*.

**Note**  To reduce exposure to security attacks, always use a format string for **Format**.
For example, **Format(input)** is exploitable, and **Format("%s", input)** is not.
Never use a user-supplied string for the format string.
If your format string  is stored for a purpose such as localization, ensure that the string is protected from unauthorized write access.
If your function writes to a string rather than standard output, you may need to avoid using a trailing "%s" in the format string.

If the string object is offered as a parameter to **Format**, the call fails.
For example, the following code causes unpredictable results.

## Examples

```cpp
CHString str = L"Some Data";

// Attention: str is also used in the parameter list.
str.Format(L"%s%d", str, 123); 
```

**Note**  When you pass a character string as an optional argument, you must cast it explicitly as **LPCWSTR**.
The format argument has the same form and function as the *format* argument for the **printf** function.
A **NULL** character is appended to the end of the written characters.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>

<a href="/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">CHString::GetBuffer</a>
