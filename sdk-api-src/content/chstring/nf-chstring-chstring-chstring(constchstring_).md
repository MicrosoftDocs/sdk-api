---
UID: NF:chstring.CHString.CHString(constCHString&)
title: CHString::CHString(const CHString &) (chstring.h)
description: Initializes a new CHString object with the specified data.
helpviewer_keywords: ["??0CHString@@QAE@ABV0@@Z","??0CHString@@QEAA@AEBV0@@Z","CHString","CHString constructor [Windows Management Instrumentation]","CHString constructor [Windows Management Instrumentation]","CHString interface","CHString interface [Windows Management Instrumentation]","CHString constructor","CHString.CHString","CHString.CHString(const CHString &)","CHString::CHString","CHString::CHString(const CHString &)","CHString::CHString(const CHString&)","chstring/CHString::CHString","wmi.chstring_chstring_const_chstring__"]
old-location: wmi\chstring_chstring_const_chstring__.htm
tech.root: wmi
ms.assetid: 2b799ee3-e54f-4911-ac0c-4bca91a830d4
ms.date: 12/05/2018
ms.keywords: ??0CHString@@QAE@ABV0@@Z, ??0CHString@@QEAA@AEBV0@@Z, CHString, CHString constructor [Windows Management Instrumentation], CHString constructor [Windows Management Instrumentation],CHString interface, CHString interface [Windows Management Instrumentation],CHString constructor, CHString.CHString, CHString.CHString(const CHString &), CHString::CHString, CHString::CHString(const CHString &), CHString::CHString(const CHString&), chstring/CHString::CHString, wmi.chstring_chstring_const_chstring__
f1_keywords:
- chstring/CHString.CHString
dev_langs:
- c++
req.header: chstring.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CHString.CHString
- ??0CHString@@QAE@ABV0@@Z
- ??0CHString@@QEAA@AEBV0@@Z
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHString::CHString(const CHString &)


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Each of these constructors initializes a new <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> object with the specified data.


## -parameters




### -param stringSrc

The existing <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> object that is copied into this <b>CHString</b> object.


## -remarks



Because the constructors copy the input data into new allocated storage, memory exceptions can result. Some of these constructors act as conversion functions; you can substitute, for example, an <b>LPWSTR</b> where a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> object is expected.

Several forms of the constructor have special purposes:

<ul>
<li>
CHString( LPCSTR
      <i>lpsz</i> )

Constructs a Unicode <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string from an ANSI string.

</li>
<li>
CHString( LPCWSTR
      <i>lpsz</i> )

Constructs a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string from a Unicode string.

</li>
<li>
CHString( const unsigned char*
      <i>lpsz</i> )

Enables you to construct a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string from a pointer to unsigned char.

</li>
</ul>

#### Examples

The following code example shows how to use <a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-chstring(constchstring_)">CHString::CHString</a>.


```cpp
CHString s1;                    // Empty string
CHString s2( L"cat" );          // From a C string literal
CHString s3 = s2;               // Copy constructor
CHString s4( s2 + " " + s3 );   // From a string expression

CHString s5( 'x' );             // s5 = "x"
CHString s6( 'x', 6 );          // s6 = "xxxxxx"

CHString city = L"Philadelphia"; // NOT the assignment operator
```




