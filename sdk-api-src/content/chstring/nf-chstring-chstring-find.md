---
UID: NF:chstring.CHString.Find
title: CHString::Find
description: 
ms.assetid: 
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: CHString::Find
ms.topic: language-reference
targetos: Windows
product: Windows
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
 - COM
api_location:
 - chstring.h
api_name:
 - CHString::Find
---

# CHString::Find

## -description

<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new development.]

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

<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>

<a href="https://msdn.microsoft.com/941c9eb3-a5b8-42b7-bb9f-732eaf1faa24">CHString::ReverseFind</a>

<a href="https://msdn.microsoft.com/f3f9111d-9191-4ba5-877a-736e11d0a168">CHString::FindOneOf</a>