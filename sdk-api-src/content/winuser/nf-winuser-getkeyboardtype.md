---
UID: NF:winuser.GetKeyboardType
title: GetKeyboardType function (winuser.h)
description: Retrieves information about the current keyboard.
helpviewer_keywords: ["GetKeyboardType","GetKeyboardType function [Keyboard and Mouse Input]","_win32_getkeyboardtype","base.getkeyboardtype","inputdev.getkeyboardtype","winui.getkeyboardtype","winuser/GetKeyboardType"]
old-location: inputdev\getkeyboardtype.htm
tech.root: inputdev
ms.assetid: 39b9ba8b-0cab-465c-9a58-2b69eea7de76
ms.date: 02/25/2021
ms.keywords: GetKeyboardType, GetKeyboardType function [Keyboard and Mouse Input], _win32_getkeyboardtype, base.getkeyboardtype, inputdev.getkeyboardtype, winui.getkeyboardtype, winuser/GetKeyboardType
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GetKeyboardType
 - winuser/GetKeyboardType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-1-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - GetKeyboardType
---

# GetKeyboardType function


## -description

Retrieves information about the current keyboard.

## -parameters

### -param nTypeFlag [in]

Type: <b>int</b>

The type of keyboard information to be retrieved. This parameter can be one of the following values.

| Value | Meaning                                     |
|:-----:|---------------------------------------------|
|   0   | Keyboard type                               |
|   1   | Keyboard subtype                            |
|   2   | The number of function keys on the keyboard |

## -returns

Type: <b>int</b>

If the function succeeds, the return value specifies the requested information.

If the function fails and <i>nTypeFlag</i> is not 1, the return value is 0; 0 is a valid return value when <i>nTypeFlag</i> is 1 (keyboard subtype). To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Valid keyboard types are:

| Value | Description                                          |
|:-----:|------------------------------------------------------|
|  0x4  | Enhanced 101- or 102-key keyboards (and compatibles) |
|  0x7  | Japanese Keyboard                                    |
|  0x8  | Korean Keyboard                                      |
| 0x51  | Unknown type or HID keyboard                         |

Keyboard subtypes are original equipment manufacturer (OEM)-dependent values.

## -see-also

<a href="/windows/desktop/inputdev/keyboard-input-functions">Keyboard Input Functions</a>
