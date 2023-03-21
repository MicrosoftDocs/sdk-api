---
UID: NF:chstring.CHString.CHString(LPCWSTR)
title: CHString::CHString(LPCWSTR) (chstring.h)
description: Initializes a new CHString object with the specified data. (overload 1/6)
helpviewer_keywords: ["??0CHString@@QAE@PBG@Z","??0CHString@@QEAA@PEBG@Z","CHString","CHString constructor [Windows Management Instrumentation]","CHString constructor [Windows Management Instrumentation]","CHString interface","CHString interface [Windows Management Instrumentation]","CHString constructor","CHString.CHString","CHString.CHString(LPCWSTR)","CHString::CHString","CHString::CHString(LPCWSTR)","chstring/CHString::CHString","wmi.chstring_chstring_lpcwstr_"]
old-location: wmi\chstring_chstring_lpcwstr_.htm
tech.root: wmi
ms.assetid: 11780ce1-b7d8-4a79-89fc-656ea5d71048
ms.date: 12/05/2018
ms.keywords: ??0CHString@@QAE@PBG@Z, ??0CHString@@QEAA@PEBG@Z, CHString, CHString constructor [Windows Management Instrumentation], CHString constructor [Windows Management Instrumentation],CHString interface, CHString interface [Windows Management Instrumentation],CHString constructor, CHString.CHString, CHString.CHString(LPCWSTR), CHString::CHString, CHString::CHString(LPCWSTR), chstring/CHString::CHString, wmi.chstring_chstring_lpcwstr_
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHString::CHString
 - chstring/CHString::CHString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.CHString
 - ??0CHString@@QAE@PBG@Z
 - ??0CHString@@QEAA@PEBG@Z
---

# CHString::CHString(LPCWSTR)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Each of these constructors initializes a new <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object with the specified data.

## -parameters

### -param lpsz

A <b>NULL</b>-terminated string that is copied into this <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object.

## -remarks

Because the constructors copy the input data into new allocated storage, memory exceptions can result. Some of these constructors act as conversion functions; you can substitute, for example, an <b>LPWSTR</b> where a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object is expected.

Several forms of the constructor have special purposes:

<ul>
<li>
CHString( LPCSTR
      <i>lpsz</i> )

Constructs a Unicode <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string from an ANSI string.

</li>
<li>
CHString( LPCWSTR
      <i>lpsz</i> )

Constructs a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string from a Unicode string.

</li>
<li>
CHString( const unsigned char*
      
      <i>psz</i>)

Enables you to construct a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string from a pointer to unsigned char.

</li>
</ul>

#### Examples

The following code example shows how to use <a href="/windows/desktop/api/chstring/nf-chstring-chstring-chstring(constchstring_)">CHString::CHString</a>.


```cpp
CHString s1;                    // Empty string
CHString s2( L"cat" );          // From a C string literal
CHString s3 = s2;               // Copy constructor
CHString s4( s2 + " " + s3 );   // From a string expression

CHString s5( 'x' );             // s5 = "x"
CHString s6( 'x', 6 );          // s6 = "xxxxxx"

CHString city = L"Philadelphia"; // NOT the assignment operator
```
