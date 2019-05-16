---
UID: NF:chstring.operator-less-than~r1
title: operator<
description: 
ms.assetid: bcd0b4a1-4fd1-4d90-b56c-485f1a09f806
ms.author: windowssdkdev
ms.date: 05/20/2019
ms.keywords: operator<
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
 - 
api_location:
 - chstring.h
api_name:
 - operator<
---

# operator<

## -description

<p class="CCE_Message">
[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new development.]

The **CHString** comparison operators compare two strings.
These operators are a convenient substitute for the case-sensitive <a href="https://msdn.microsoft.com/6e587dd3-b3ae-4afa-9582-b3867d2fb7ef">Compare</a> method.

## -parameters

### -param s1

Reference to the CHString to the left of the operator for this comparison.

### -param s2

Reference to the null-terminated string to the right of the operator for this comparison.

## -returns

## -remarks

#### Examples

The following code example shows the use of a CHString Comparison Operator:

```cpp
CHString s1( L"abc" );
LPCWSTR s2( L"abd" );

assert( s1 < s2 );
```

## -see-also

<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>
