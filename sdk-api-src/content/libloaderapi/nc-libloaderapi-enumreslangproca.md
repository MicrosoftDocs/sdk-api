---
UID: NC:libloaderapi.ENUMRESLANGPROCA
title: ENUMRESLANGPROCA (libloaderapi.h)
description: An application-defined callback function used with the EnumResourceLanguages and EnumResourceLanguagesEx functions. (ANSI)
helpviewer_keywords: ["EnumResLangProc","EnumResLangProc callback","EnumResLangProc callback function [Menus and Other Resources]","EnumResLangProcA","EnumResLangProcW","_win32_EnumResLangProc","_win32_enumreslangproc_cpp","libloaderapi/EnumResLangProc","libloaderapi/EnumResLangProcA","libloaderapi/EnumResLangProcW","menurc.enumreslangproc","winui._win32_enumreslangproc"]
old-location: menurc\enumreslangproc.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumreslangproc.htm
ms.date: 05/17/2023
ms.keywords: EnumResLangProc, EnumResLangProc callback, EnumResLangProc callback function [Menus and Other Resources], EnumResLangProcA, EnumResLangProcW, _win32_EnumResLangProc, _win32_enumreslangproc_cpp, libloaderapi/EnumResLangProc, libloaderapi/EnumResLangProcA, libloaderapi/EnumResLangProcW, menurc.enumreslangproc, winui._win32_enumreslangproc
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResLangProcW (Unicode) and EnumResLangProcA (ANSI)
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
 - ENUMRESLANGPROCW
 - libloaderapi/ENUMRESLANGPROCW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - libloaderapi.h
api_name:
 - EnumResLangProc
 - EnumResLangProcA
 - EnumResLangProcW
---

## -description

An application-defined callback function used with the [**EnumResourceLanguagesA**](../winbase/nf-winbase-enumresourcelanguagesa.md) and the [**EnumResourceLanguagesExA**](nf-libloaderapi-enumresourcelanguagesexa.md) functions. It receives the type, name, and language of a resource item. The **ENUMRESLANGPROC** type defines a pointer to this callback function. *EnumResLangProc* is a placeholder for the application-defined function name.

## Syntax

``` c++
BOOL CALLBACK EnumResLangProc(
  _In_opt_ HMODULE  hModule,
  _In_     LPCSTR  lpszType,
  _In_     LPCSTR  lpszName,
  _In_     WORD     wIDLanguage,
  _In_     LONG_PTR lParam
);
```

## -parameters

### -param hModule [in, optional]

Type: **HMODULE**

A handle to the module whose executable file contains the resources for which the languages are being enumerated. If this parameter is **NULL**, the function enumerates the resource languages in the module used to create the current process.

### -param lpType [in]

Type: **LPCSTR**

The type of resource for which the language is being enumerated. Alternately, rather than a pointer, this parameter can be [**MAKEINTRESOURCE**](../winuser/nf-winuser-makeintresourcea.md)(ID), where ID is an integer value representing a predefined resource type. For standard resource types, see [Resource Types](/windows/win32/menurc/resource-types). For more information, see the Remarks section below.

### -param lpName [in]

Type: **LPCSTR**

The name of the resource for which the language is being enumerated. Alternately, rather than a pointer, this parameter can be [**MAKEINTRESOURCE**](../winuser/nf-winuser-makeintresourcea.md)(ID), where ID is the integer identifier of the resource. For more information, see the Remarks section below.

### -param wLanguage [in]

Type: **WORD**

The language identifier for the resource for which the language is being enumerated. The [**EnumResourceLanguagesA**](../winbase/nf-winbase-enumresourcelanguagesa.md) or [**EnumResourceLanguagesExA**](nf-libloaderapi-enumresourcelanguagesexa.md) function provides this value. For a list of the primary language identifiers and sublanguage identifiers that constitute a language identifier, see [**MAKELANGID**](../winnt/nf-winnt-makelangid.md).

### -param lParam [in]

Type: **LONG\_PTR**

The application-defined parameter passed to the [**EnumResourceLanguagesA**](../winbase/nf-winbase-enumresourcelanguagesa.md) or [**EnumResourceLanguagesExA**](nf-libloaderapi-enumresourcelanguagesexa.md) function. This parameter can be used in error checking.

## -returns

Type: **BOOL**

Returns **TRUE** to continue enumeration or **FALSE** to stop enumeration.

## Remarks

If [**IS_INTRESOURCE**](../winuser/nf-winuser-is_intresource.md)(*lpszType*) is **TRUE**, then *lpszType* specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (\#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource type. For example, the string "\#258" represents the identifier 258.

Similarly, if [**IS_INTRESOURCE**](../winuser/nf-winuser-is_intresource.md)(*lpszName*) is **TRUE**, then *lpszName* specifies the integer identifier of the given resource. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (\#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource.

An application must register this function by passing its address to the [**EnumResourceLanguagesA**](../winbase/nf-winbase-enumresourcelanguagesa.md) or [**EnumResourceLanguagesExA**](nf-libloaderapi-enumresourcelanguagesexa.md) function.

If the callback function returns **FALSE**, then [**EnumResourceLanguagesA**](../winbase/nf-winbase-enumresourcelanguagesa.md) or [**EnumResourceLanguagesExA**](nf-libloaderapi-enumresourcelanguagesexa.md) will stop enumeration and return **FALSE**. The value obtained from [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) will be **ERROR\_RESOURCE\_ENUM\_USER\_STOP**.

## See also

[**EnumResourceLanguagesA**](../winbase/nf-winbase-enumresourcelanguagesa.md)

[**EnumResourceLanguagesExA**](nf-libloaderapi-enumresourcelanguagesexa.md)

[**IS_INTRESOURCE**](../winuser/nf-winuser-is_intresource.md)

[**MAKELANGID**](../winnt/nf-winnt-makelangid.md)

[Resources](/windows/win32/menurc/resources)
