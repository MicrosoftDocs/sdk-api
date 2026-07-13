---
UID: NF:winuser.EnumPropsExW
title: EnumPropsExW function (winuser.h)
description: Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. EnumPropsEx continues until the last entry is enumerated or the callback function returns FALSE. (Unicode)
helpviewer_keywords: ["EnumPropsEx", "EnumPropsEx function [Windows and Messages]", "EnumPropsExW", "_win32_EnumPropsEx", "_win32_enumpropsex_cpp", "winmsg.enumpropsex", "winui._win32_enumpropsex", "winuser/EnumPropsEx", "winuser/EnumPropsExW"]
old-location: winmsg\enumpropsex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\enumpropsex.htm
ms.date: 12/05/2018
ms.keywords: EnumPropsEx, EnumPropsEx function [Windows and Messages], EnumPropsExA, EnumPropsExW, _win32_EnumPropsEx, _win32_enumpropsex_cpp, winmsg.enumpropsex, winui._win32_enumpropsex, winuser/EnumPropsEx, winuser/EnumPropsExA, winuser/EnumPropsExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumPropsExW (Unicode) and EnumPropsExA (ANSI)
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
 - EnumPropsExW
 - winuser/EnumPropsExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
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
 - EnumPropsEx
 - EnumPropsExA
 - EnumPropsExW
---

# EnumPropsExW function


## -description

Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. <b>EnumPropsEx</b> continues until the last entry is enumerated or the callback function returns <b>FALSE</b>.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is to be enumerated.

### -param lpEnumFunc [in]

Type: <b>PROPENUMPROCEX</b>

A pointer to the callback function. For more information about the callback function, see the <a href="/windows/desktop/api/winuser/nc-winuser-propenumprocexw">PropEnumProcEx</a> function.

### -param lParam [in]

Type: <b>LPARAM</b>

Application-defined data to be passed to the callback function.

## -returns

Type: <b>int</b>

The return value specifies the last value returned by the callback function. It is -1 if the function did not find a property for enumeration.

## -remarks

An application can remove only those properties it has added. It must not remove properties added by other applications or by the system itself. 


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-window-properties">Listing Window Properties for a Given Window</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines EnumPropsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nc-winuser-propenumprocexa">PropEnumProcEx</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/window-properties">Window Properties</a>
