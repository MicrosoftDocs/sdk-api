---
UID: NC:winuser.PROPENUMPROCA
title: PROPENUMPROCA (winuser.h)
description: An application-defined callback function used with the EnumProps function. (ANSI)
helpviewer_keywords: ["PropEnumProc","PropEnumProc callback","PropEnumProc callback function [Windows and Messages]","PropEnumProcA","PropEnumProcW","_win32_PropEnumProc","_win32_propenumproc_cpp","winmsg.propenumproc","winui._win32_propenumproc","winuser/PropEnumProc","winuser/PropEnumProcA","winuser/PropEnumProcW"]
old-location: winmsg\propenumproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\propenumproc.htm
ms.date: 09/30/2025
ms.keywords: PropEnumProc, PropEnumProc callback, PropEnumProc callback function [Windows and Messages], PropEnumProcA, PropEnumProcW, _win32_PropEnumProc, _win32_propenumproc_cpp, winmsg.propenumproc, winui._win32_propenumproc, winuser/PropEnumProc, winuser/PropEnumProcA, winuser/PropEnumProcW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: PropEnumProcW (Unicode) and PropEnumProcA (ANSI)
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
 - PROPENUMPROCA
 - winuser/PROPENUMPROCA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - PropEnumProc
 - PropEnumProcA
 - PropEnumProcW
---

# PROPENUMPROCA callback function

## -description

An application-defined callback function used with the [EnumProps](/windows/desktop/api/winuser/nf-winuser-enumpropsa) function. The function receives property entries from a window's property list. The **PROPENUMPROC** type defines a pointer to this callback function. _PropEnumProc_ is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: **HWND**

A handle to the window whose property list is being enumerated. This parameter is typically named _hWnd_.

### -param unnamedParam2

Type: **LPCTSTR**

The string component of a property list entry. This is the string that was specified, along with a data handle, when the property was added to the window's property list via a call to the [SetProp](/windows/desktop/api/winuser/nf-winuser-setpropa) function. This parameter is typically named _lpString_.

### -param unnamedParam3

Type: **HANDLE**

A handle to the data. This handle is the data component of a property list entry. This parameter is typically named _hData_.

## -returns

Type: **BOOL**

Return **TRUE** to continue the property list enumeration.

Return **FALSE** to stop the property list enumeration.

## -remarks

> [!NOTE]
> The parameters are defined in the header with no names: `typedef BOOL (CALLBACK* PROPENUMPROCA)(HWND, LPCSTR, HANDLE);`. Therefore, the syntax block lists them as `unnamedParam1` - `unnamedParam3`. You can name these parameters anything in your app. However, they are usually named as shown in the parameter descriptions.

The following restrictions apply to this callback function:

- The callback function can call the [RemoveProp](/windows/desktop/api/winuser/nf-winuser-removepropa) function. However, **RemoveProp** can remove only the property passed to the callback function through the callback function's parameters.
- The callback function should not attempt to add properties.

> [!NOTE]
> The winuser.h header defines PROPENUMPROC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

**Conceptual**

[Window Properties](/windows/desktop/winmsg/window-properties)

**Reference**

[EnumProps](/windows/desktop/api/winuser/nf-winuser-enumpropsa)

[RemoveProp](/windows/desktop/api/winuser/nf-winuser-removepropa)

[SetProp](/windows/desktop/api/winuser/nf-winuser-setpropa)
