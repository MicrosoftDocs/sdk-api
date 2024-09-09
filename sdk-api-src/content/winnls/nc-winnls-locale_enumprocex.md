---
UID: NC:winnls.LOCALE_ENUMPROCEX
title: LOCALE_ENUMPROCEX (winnls.h)
description: An application-defined callback function that processes enumerated locale information provided by the EnumSystemLocalesEx function.
helpviewer_keywords: ["EnumLocalesProcEx","LOCALE_ENUMPROCEX","LOCALE_ENUMPROCEX callback","LOCALE_ENUMPROCEX callback function [Internationalization for Windows Applications]","_win32_EnumLocalesProcEx","intl.enumlocalesprocex","winnls/LOCALE_ENUMPROCEX"]
old-location: intl\enumlocalesprocex.htm
tech.root: Intl
ms.date: 12/05/2018
ms.keywords: EnumLocalesProcEx, LOCALE_ENUMPROCEX, LOCALE_ENUMPROCEX callback, LOCALE_ENUMPROCEX callback function [Internationalization for Windows Applications], _win32_EnumLocalesProcEx, intl.enumlocalesprocex, winnls/LOCALE_ENUMPROCEX
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LOCALE_ENUMPROCEX
 - winnls/LOCALE_ENUMPROCEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNls.h
api_name:
 - LOCALE_ENUMPROCEX
---

# LOCALE_ENUMPROCEX callback function


## -description

An application-defined callback function that processes enumerated locale information provided by the <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a> function. The LOCALE_ENUMPROCEX type defines a pointer to this callback function. **EnumLocalesProcEx** is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Pointer to a buffer containing a null-terminated [locale name](/windows/win32/intl/locale-names) string.

### -param unnamedParam2

Flags defining locale information. Values for this parameter can include a binary OR of flags, but some flag combinations never occur. If the application specifies [LOCALE_WINDOWS](/windows/win32/intl/locale-windows) or [LOCALE_ALTERNATE_SORTS](/windows/win32/intl/locale-alternate-sorts), it can also specify [LOCALE_REPLACEMENT](/windows/win32/intl/locale-replacement) so that the [EnumSystemLocalesEx](./nf-winnls-enumsystemlocalesex.md) function can test to see if the locale is a replacement.

- [LOCALE_ALL](/windows/win32/intl/locale-all)
- [LOCALE_ALTERNATE_SORTS](/windows/win32/intl/locale-alternate-sorts); for more information, see [EnumSystemLocalesEx](./nf-winnls-enumsystemlocalesex.md)
- [LOCALE_NEUTRALDATA](/windows/win32/intl/locale-neutraldata)
- [LOCALE_REPLACEMENT](/windows/win32/intl/locale-replacement) This constant is not a valid input to the *dwFlags* parameter of <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>. To enumerate replacement locales, the application should call this function with the *Arg2* parameter specified as **LOCALE_WINDOWS** or **LOCALE_ALL**, then check for this constant in the callback function.
- [LOCALE_SUPPLEMENTAL](/windows/win32/intl/locale-supplemental)
- [LOCALE_WINDOWS](/windows/win32/intl/locale-windows)
- [LOCALE_NEUTRALDATA](/windows/win32/intl/locale-neutraldata)
- [LOCALE_SPECIFICDATA](/windows/win32/intl/locale-specificdata)

### -param unnamedParam3

An application-provided input parameter of <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>. This value is especially useful for multi-threaded applications, since it can be used to pass thread-specific data to this callback function.

## -returns

Returns **TRUE** to continue enumeration or **FALSE** otherwise.

## -remarks

An **EnumLocalesProcEx** function can carry out any desired task. The application registers this function by passing its address to the <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a> function.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
