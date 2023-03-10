---
UID: NF:chstring.operator-less-than-equal-to
title: operator<=
description: The chstring.operator-less-than-equal-to function compares two strings. These operators are a convenient substitute for the case-sensitive Compare method.
tech.root: wmi
helpviewer_keywords: ["operator<="]
ms.assetid: 21a19f00-67ec-4bf2-b429-44e9463732e4
ms.date: 08/10/2022
ms.keywords: operator<=
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
 - operator<=
 - chstring/operator<=
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - chstring.h
api_name:
 - operator<=
---

# operator<=


## -description

<p class="CCE_Message">
[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new development.]

The **CHString** comparison operators compare two strings.
These operators are a convenient substitute for the case-sensitive <a href="/windows/desktop/api/chstring/nf-chstring-chstring-compare">Compare</a> method.

## -parameters

### -param s1

Reference to the **CHString** to the left of the operator for this comparison.

### -param s2

Reference to the **CHString** to the right of the operator for this comparison.

## -returns

If the strings meet the comparison condition, the operators return a nonzero value.
Otherwise, 0 is returned.

## -remarks

#### Examples

The following code example shows the use of a **CHString** Comparison Operator:

```cpp
CHString s1( L"abc" );
CHString s2( L"abd" );

assert( s1 <= s2 );
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>