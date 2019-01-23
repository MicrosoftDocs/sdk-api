---
UID: NF:chstring.CHString.CHString(const unsigned char)
title: CHString::CHString(const unsigned char)
author: windows-sdk-content
description: Initializes a new CHString object with the specified data.
old-location: wmi\chstring_chstring_const_unsigned_char__.htm
tech.root: WmiSdk
ms.assetid: aa1cf180-bc7c-40ba-91ab-091018790b39
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "??0CHString@@QAE@PBE@Z, ??0CHString@@QEAA@PEBE@Z, CHString, CHString constructor [Windows Management Instrumentation], CHString constructor [Windows Management Instrumentation],CHString interface, CHString interface [Windows Management Instrumentation],CHString constructor, CHString.CHString, CHString.CHString(const unsigned char), CHString::CHString, CHString::CHString(const unsigned char), CHString::CHString(const unsigned char*), chstring/CHString::CHString, wmi.chstring_chstring_const_unsigned_char__"
ms.topic: method
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
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.CHString
 - ??0CHString@@QAE@PBE@Z
 - ??0CHString@@QEAA@PEBE@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::CHString(const unsigned char)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Each of these constructors initializes a new <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object with the specified data.


## -parameters




### -param lpsz

A <b>NULL</b>-terminated string that is copied into this <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object.


## -remarks



Because the constructors copy the input data into new allocated storage, memory exceptions can result. Some of these constructors act as conversion functions; you can substitute, for example, an <b>LPWSTR</b> where a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object is expected.

Several forms of the constructor have special purposes:

<ul>
<li>
CHString( LPCSTR
      <i>lpsz</i> )

Constructs a Unicode <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string from an ANSI string.

</li>
<li>
CHString( LPCWSTR
      <i>lpsz</i> )

Constructs a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string from a Unicode string.

</li>
<li>
CHString( const unsigned char*
      <i>psz</i> )

Enables you to construct a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string from a pointer to unsigned char.

</li>
</ul>

#### Examples

The following code example shows how to use <a href="https://msdn.microsoft.com/d49e1600-d5d4-4c44-81c5-1b8c53b768de">CHString::CHString</a>.


```cpp
CHString s1;                    // Empty string
CHString s2( L"cat" );          // From a C string literal
CHString s3 = s2;               // Copy constructor
CHString s4( s2 + " " + s3 );   // From a string expression

CHString s5( 'x' );             // s5 = "x"
CHString s6( 'x', 6 );          // s6 = "xxxxxx"

CHString city = L"Philadelphia"; // NOT the assignment operator
```




