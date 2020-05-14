---
UID: NF:chstring.CHString.Find(WCHAR)
title: CHString::Find
description: helpviewer_keywords: ["CHString::Find"]
ms.assetid: 
ms.date: 05/13/2019
ms.keywords: CHString::Find
f1_keywords:
- chstring/CHString::Find
dev_langs:
- c++
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
topic_type:
- apiref
api_type:
- DllExport
api_location:
- chstring.h
api_name:
- CHString::Find
---

# CHString::Find

## -description

<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new development.]

The **Find** method searches a string for the first match of a substring.

## -parameters

### -param ch

A single character that the method searches for.

## -returns

If the **Find** method is successful, it returns the zero-based index of the first character in this **CHString** string that matches the requested substring or characters.
If the substring or character is not found, the method returns a value of -1.

## -remarks

The **Find** method is overloaded to accept both single characters (similar to the runtime function, **wcschr**) and strings (similar to the runtime function, **wcsstr**).

#### Examples

The following code example shows the use of **CHString::Find**.

```cpp
CHString s( L"abcdef" );
assert( s.Find( 'c' ) == 2 );
assert( s.Find( L"de" ) == 3 );
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a>

<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-reversefind">CHString::ReverseFind</a>

<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-findoneof">CHString::FindOneOf</a>
