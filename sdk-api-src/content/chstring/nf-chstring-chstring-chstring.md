---
UID: NF:chstring.CHString.CHString
title: CHString::CHString
description: The CHString::CHString function initializes a new CHString object with the specified data.
tech.root: wmi
helpviewer_keywords: ["CHString::CHString"]
ms.assetid: cb7da79b-f808-4f2d-ac33-559fdc9a9978
ms.date: 08/10/2022
ms.keywords: CHString::CHString
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
 - CHString::CHString
 - chstring/CHString::CHString
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - chstring.h
api_name:
 - CHString::CHString
---

# CHString::CHString


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.
The <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new development.]

Each of these constructors initializes a new **CHString** object with the specified data.



## -remarks

Because the constructors copy the input data into new allocated storage, memory exceptions can result.
Some of these constructors act as conversion functions; you can substitute, for example, an **LPWSTR** where a **CHString** object is expected.

- CHString( LPCSTR *lpsz* )
Constructs a Unicode **CHString** string from an ANSI string.
- CHString( LPCWSTR *lpsz* )
Constructs a **CHString** string from a Unicode string.
- CHString( const unsigned char* *psz* )
Enables you to construct a **CHString** string from a pointer to unsigned char.

#### Examples

The following code example shows the use of <a href="/windows/desktop/api/chstring/nf-chstring-chstring-chstring(constchstring_)">CHString::CHString</a>:

```cpp
CHString s1;                    // Empty string
CHString s2( L"cat" );          // From a C string literal
CHString s3 = s2;               // Copy constructor
CHString s4( s2 + " " + s3 );   // From a string expression

CHString s5( 'x' );             // s5 = "x"
CHString s6( 'x', 6 );          // s6 = "xxxxxx"

CHString city = L"Philadelphia"; // NOT the assignment operator
```

## -see-also
