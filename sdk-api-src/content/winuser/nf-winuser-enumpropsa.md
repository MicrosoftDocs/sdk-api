---
UID: NF:winuser.EnumPropsA
title: EnumPropsA function (winuser.h)
description: Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. EnumProps continues until the last entry is enumerated or the callback function returns FALSE. (ANSI)
helpviewer_keywords: ["EnumPropsA", "winuser/EnumPropsA"]
old-location: winmsg\enumprops.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\enumprops.htm
ms.date: 12/05/2018
ms.keywords: EnumProps, EnumProps function [Windows and Messages], EnumPropsA, EnumPropsW, _win32_EnumProps, _win32_enumprops_cpp, winmsg.enumprops, winui._win32_enumprops, winuser/EnumProps, winuser/EnumPropsA, winuser/EnumPropsW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumPropsW (Unicode) and EnumPropsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumPropsA
 - winuser/EnumPropsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - ext-ms-win-ntuser-window-l1-1-4.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - ext-ms-win-ntuser-window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-0.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - EnumProps
 - EnumPropsA
 - EnumPropsW
---

# EnumPropsA function


## -description

Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. <b>EnumProps</b> continues until the last entry is enumerated or the callback function returns <b>FALSE</b>.

To pass application-defined data to the callback function, use <a href="/windows/desktop/api/winuser/nf-winuser-enumpropsexa">EnumPropsEx</a> function.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is to be enumerated.

### -param lpEnumFunc [in]

Type: <b>PROPENUMPROC</b>

A pointer to the callback function. For more information about the callback function, see the <a href="/windows/desktop/api/winuser/nc-winuser-propenumproca">PropEnumProc</a> function.

## -returns

Type: <b>int</b>

The return value specifies the last value returned by the callback function. It is -1 if the function did not find a property for enumeration.

## -remarks

An application can remove only those properties it has added. It must not remove properties added by other applications or by the system itself. 





> [!NOTE]
> The winuser.h header defines EnumProps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enumpropsexa">EnumPropsEx</a>



<a href="/windows/desktop/api/winuser/nc-winuser-propenumproca">PropEnumProc</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/window-properties">Window Properties</a>
