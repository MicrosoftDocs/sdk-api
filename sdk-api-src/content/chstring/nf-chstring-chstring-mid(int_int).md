---
UID: NF:chstring.CHString.Mid(int,int)
title: CHString::Mid
description: The CHString::Mid method extracts a substring of length nCount characters from a CHString string, starting at position nFirst (zero-based). 
tech.root: wmi
helpviewer_keywords: ["CHString::Mid"]
ms.assetid: f79f7b70-0587-4d5d-8a18-c61bd3c69212
ms.date: 08/10/2022
ms.keywords: CHString::Mid
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
 - CHString::Mid
 - chstring/CHString::Mid
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - chstring.h
api_name:
 - CHString::Mid
---

# CHString::Mid


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new development.]

The **Mid** method extracts a substring of length *nCount* characters from a **CHString** string, starting at position *nFirst* (zero-based).
The method returns a copy of the extracted substring.

## -parameters

### -param nFirst

The zero-based index of the first character in this <wdcml:xref targtype="object" rid="wmi.chstring" xmlns:wdcml="http://microsoft.com/wdcml">CHString</wdcml:xref> string that is be included in the extracted substring.

### -param nCount

The number of characters to extract form this **CHString** string.
If this parameter is not supplied, then the remainder of the string is extracted.

## -returns

Returns a **CHString** object that contains a copy of the specified range of characters.
The returned **CHString** object may be empty.

CHeap_Exception

## -remarks

The **Mid** method is similar to the Basic **MID$** function except in the Basic MID$ function, indexes are zero-based.

The following code example shows the use of **CHString::Mid**.

```cpp
CHString s( L"abcdef" );
assert( s.Mid( 2, 3 ) == L"cde" );
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>

<a href="/windows/desktop/api/chstring/nf-chstring-chstring-left">CHString::Left</a>

<a href="/windows/desktop/api/chstring/nf-chstring-chstring-right">CHString::Right</a>