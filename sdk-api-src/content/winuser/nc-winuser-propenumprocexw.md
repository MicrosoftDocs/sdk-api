---
UID: NC:winuser.PROPENUMPROCEXW
title: PROPENUMPROCEXW (winuser.h)
description: Application-defined callback function used with the EnumPropsEx function. (Unicode)
helpviewer_keywords: ["PropEnumProcEx","PropEnumProcEx callback","PropEnumProcEx callback function [Windows and Messages]","PropEnumProcExA","PropEnumProcExW","_win32_PropEnumProcEx","_win32_propenumprocex_cpp","winmsg.propenumprocex","winui._win32_propenumprocex","winuser/PropEnumProcEx","winuser/PropEnumProcExA","winuser/PropEnumProcExW"]
old-location: winmsg\propenumprocex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\propenumprocex.htm
ms.date: 09/30/2025
ms.keywords: PropEnumProcEx, PropEnumProcEx callback, PropEnumProcEx callback function [Windows and Messages], PropEnumProcExA, PropEnumProcExW, _win32_PropEnumProcEx, _win32_propenumprocex_cpp, winmsg.propenumprocex, winui._win32_propenumprocex, winuser/PropEnumProcEx, winuser/PropEnumProcExA, winuser/PropEnumProcExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: PropEnumProcExW (Unicode) and PropEnumProcExA (ANSI)
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
 - PROPENUMPROCEXW
 - winuser/PROPENUMPROCEXW
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
 - PropEnumProcEx
 - PropEnumProcExA
 - PropEnumProcExW
---

# PROPENUMPROCEXW callback function

## -description

Application-defined callback function used with the [EnumPropsEx](/windows/desktop/api/winuser/nf-winuser-enumpropsexw) function. The function receives property entries from a window's property list. The PROPENUMPROCEX type defines a pointer to this callback function. **PropEnumProcEx** is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: **HWND**

A handle to the window whose property list is being enumerated. This parameter is typically named _hWnd_.

### -param unnamedParam2

Type: **LPWSTR**

The string component of a property list entry. This is the string that was specified, along with a data handle, when the property was added to the window's property list via a call to the [SetProp](/windows/desktop/api/winuser/nf-winuser-setpropw) function. This parameter is typically named _lpString_.

### -param unnamedParam3

Type: **HANDLE**

A  handle to the data. This handle is the data component of a property list entry. This parameter is typically named _hData_.

### -param unnamedParam4

Type: **ULONG_PTR**

Application-defined data. This is the value that was specified as the _lParam_ parameter of the call to [EnumPropsEx](/windows/desktop/api/winuser/nf-winuser-enumpropsexw) that initiated the enumeration. This parameter is typically named _dwData_.

## -returns

Type: **BOOL**

Return **TRUE** to continue the property list enumeration.

Return **FALSE** to stop the property list enumeration.

## -remarks

> [!NOTE]
> The parameters are defined in the header with no names: `typedef BOOL (CALLBACK* PROPENUMPROCEXW)(HWND, LPWSTR, HANDLE, ULONG_PTR);`. Therefore, the syntax block lists them as `unnamedParam1` - `unnamedParam4`. You can name these parameters anything in your app. However, they are usually named as shown in the parameter descriptions.

The following restrictions apply to this callback function:

- The callback function can call the [RemoveProp](/windows/desktop/api/winuser/nf-winuser-removepropw) function. However, **RemoveProp** can remove only the property passed to the callback function through the callback function's parameters.
- The callback function should not attempt to add properties.

> [!NOTE]
> The winuser.h header defines PROPENUMPROCEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

**Conceptual**

[Window Properties](/windows/desktop/winmsg/window-properties)

**Reference**

[EnumPropsEx](/windows/desktop/api/winuser/nf-winuser-enumpropsexw)

[RemoveProp](/windows/desktop/api/winuser/nf-winuser-removepropw)

[SetProp](/windows/desktop/api/winuser/nf-winuser-setpropw)
