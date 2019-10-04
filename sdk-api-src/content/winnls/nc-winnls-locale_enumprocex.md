---
UID: NC:winnls.LOCALE_ENUMPROCEX
title: LOCALE_ENUMPROCEX (winnls.h)
author: windows-sdk-content
description: An application-defined callback function that processes enumerated locale information provided by the EnumSystemLocalesEx function.
old-location: intl\enumlocalesprocex.htm
tech.root: Intl
ms.assetid: 583cc7bc-da1d-4dfc-83f2-2da2b304af62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumLocalesProcEx, LOCALE_ENUMPROCEX, LOCALE_ENUMPROCEX callback, LOCALE_ENUMPROCEX callback function [Internationalization for Windows Applications], _win32_EnumLocalesProcEx, intl.enumlocalesprocex, winnls/LOCALE_ENUMPROCEX
ms.topic: callback
f1_keywords: 
 - "winnls/LOCALE_ENUMPROCEX"
dev_langs:
 - c++
req.header: winnls.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNls.h
api_name:
 - LOCALE_ENUMPROCEX
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LOCALE_ENUMPROCEX callback function


## -description


An application-defined callback function that processes enumerated locale information provided by the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a> function. The LOCALE_ENUMPROCEX type defines a pointer to this callback function. <b>EnumLocalesProcEx</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - dwFlags [in]

Flags defining locale information. Values for this parameter can include a binary OR of flags, but some flag combinations never occur. If the application specifies <a href="https://docs.microsoft.com/windows/desktop/Intl/locale-windows">LOCALE_WINDOWS</a> or <a href="https://docs.microsoft.com/windows/desktop/Intl/locale-alternate-sorts">LOCALE_ALTERNATE_SORTS</a>, it can also specify <a href="https://docs.microsoft.com/windows/desktop/Intl/locale-replacement">LOCALE_REPLACEMENT</a> so that the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a> function can test to see if the locale is a replacement.


<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-all">LOCALE_ALL</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-alternate-sorts">LOCALE_ALTERNATE_SORTS</a>; for more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-neutraldata">LOCALE_NEUTRALDATA</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-replacement">LOCALE_REPLACEMENT</a>
<div class="alert"><b>Note</b>  This constant is not a valid input to the <i>dwFlags</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>. To enumerate replacement locales, the application should call this function with the <i>dwFlags</i> parameter specified as LOCALE_WINDOWS or LOCALE_ALL, then check for this constant in the callback function.</div>
<div> </div>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-supplemental">LOCALE_SUPPLEMENTAL</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-windows">LOCALE_WINDOWS</a>
</li>
</ul>

#### - lParam [in]

An application-provided input parameter of <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>. This value is especially useful for multi-threaded applications, since it can be used to pass thread-specific data to this callback function.


#### - lpLocaleString [in]

Pointer to a buffer containing a null-terminated <a href="https://docs.microsoft.com/windows/desktop/Intl/locale-names">locale name</a> string.


## -returns



Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> otherwise.




## -remarks



An <b>EnumLocalesProcEx</b> function can carry out any desired task. The application registers this function by passing its address to the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
 

 

