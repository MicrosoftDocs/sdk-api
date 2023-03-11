---
UID: NC:libloaderapi.ENUMRESTYPEPROCW
title: ENUMRESTYPEPROCW (libloaderapi.h)
description: An application-defined callback function used with the EnumResourceTypes and EnumResourceTypesEx functions. (Unicode)
helpviewer_keywords: ["EnumResTypeProc","EnumResTypeProc callback","EnumResTypeProc callback function [Menus and Other Resources]","EnumResTypeProcA","EnumResTypeProcW","_win32_EnumResTypeProc","_win32_enumrestypeproc_cpp","libloaderapi/EnumResTypeProc","libloaderapi/EnumResTypeProcA","libloaderapi/EnumResTypeProcW","menurc.enumrestypeproc","winui._win32_enumrestypeproc"]
old-location: menurc\enumrestypeproc.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumrestypeproc.htm
ms.date: 12/05/2018
ms.keywords: EnumResTypeProc, EnumResTypeProc callback, EnumResTypeProc callback function [Menus and Other Resources], EnumResTypeProcA, EnumResTypeProcW, _win32_EnumResTypeProc, _win32_enumrestypeproc_cpp, libloaderapi/EnumResTypeProc, libloaderapi/EnumResTypeProcA, libloaderapi/EnumResTypeProcW, menurc.enumrestypeproc, winui._win32_enumrestypeproc
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResTypeProcW (Unicode) and EnumResTypeProcA (ANSI)
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
 - ENUMRESTYPEPROCW
 - libloaderapi/ENUMRESTYPEPROCW
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
 - EnumResTypeProc
 - EnumResTypeProcA
 - EnumResTypeProcW
---

## -description

An application-defined callback function used with the <a href="/windows/win32/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a> and <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa">EnumResourceTypesEx</a> functions. It receives resource types. The <b>ENUMRESTYPEPROC</b> type defines a pointer to this callback function. <i>EnumResTypeProc</i> is a placeholder for the application-defined function name.

## -parameters

### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose executable file contains the resources for which the types are to be enumerated. If this parameter is <b>NULL</b>, the function enumerates the resource types in the module used to create the current process.

### -param lpType

Type: <b>LPTSTR</b>

The type of resource for which the type is being enumerated. 

Alternately, rather than a pointer, this parameter can be <a href="/windows/win32/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the given resource type. For standard resource types, see <a href="/windows/desktop/menurc/resource-types">Resource Types</a>. For more information, see the Remarks section below.

### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined parameter passed to the <a href="/windows/win32/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a> or <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa">EnumResourceTypesEx</a> function. This parameter can be used in error checking. 

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.

## -remarks

If <a href="/windows/win32/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>(<i>lpszType</i>) is <b>TRUE</b>, then <i>lpszType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

An application must register this function by passing its address to the <a href="/windows/win32/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a> or <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa">EnumResourceTypesEx</a> function. 

If the callback function returns <b>FALSE</b>, then <a href="/windows/win32/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a> or <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa">EnumResourceTypesEx</a> will stop enumeration and return <b>FALSE</b>. On Windows XP and earlier the value obtained from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will be <b>ERROR_SUCCESS</b>; starting with Windows Vista, the last error value will be <b>ERROR_RESOURCE_ENUM_USER_STOP</b>.

> [!NOTE]
> The libloaderapi.h header defines ENUMRESTYPEPROC as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/win32/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa">EnumResourceTypesEx</a>



<a href="/windows/win32/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
