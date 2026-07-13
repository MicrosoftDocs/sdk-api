---
UID: NF:winuser.GET_FLAGS_LPARAM
title: GET_FLAGS_LPARAM macro (winuser.h)
description: Retrieves the state of certain virtual keys from the specified LPARAM value. (GET_FLAGS_LPARAM)
helpviewer_keywords: ["GET_FLAGS_LPARAM","GET_FLAGS_LPARAM macro [Keyboard and Mouse Input]","_win32_GET_FLAGS_LPARAM","_win32_get_flags_lparam_cpp","inputdev.get_flags_lparam","winui._win32_get_flags_lparam","winuser/GET_FLAGS_LPARAM"]
old-location: inputdev\get_flags_lparam.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputmacros\get_flags_lparam.htm
ms.date: 07/01/2025
ms.keywords: GET_FLAGS_LPARAM, GET_FLAGS_LPARAM macro [Keyboard and Mouse Input], _win32_GET_FLAGS_LPARAM, _win32_get_flags_lparam_cpp, inputdev.get_flags_lparam, winui._win32_get_flags_lparam, winuser/GET_FLAGS_LPARAM
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GET_FLAGS_LPARAM
 - winuser/GET_FLAGS_LPARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - GET_FLAGS_LPARAM
---

# GET_FLAGS_LPARAM macro

## -syntax

```cpp
int GET_FLAGS_LPARAM(
    LPARAM lParam
);
```

## -returns

Type: **int**

The return value is the low-order word representing the virtual key state. It can be one of the following values:

| Return code | Value | Description |
|--|--|--|
| **MK_CONTROL** | 0x0008 | The CTRL key is down. |
| **MK_LBUTTON** | 0x0001 | The left mouse button is down. |
| **MK_MBUTTON** | 0x0010 | The middle mouse button is down. |
| **MK_RBUTTON** | 0x0002 | The right mouse button is down. |
| **MK_SHIFT** | 0x0004 | The SHIFT key is down. |
| **MK_XBUTTON1** | 0x0020 | The first X button is down. |
| **MK_XBUTTON2** | 0x0040 | The second X button is down. |

## -description

Retrieves the state of certain virtual keys from the specified <b>LPARAM</b> value.

## -parameters

### -param lParam

The value to be converted.

## -remarks

This macro is identical to the <a href="/windows/desktop/api/winuser/nf-winuser-get_keystate_lparam">GET_KEYSTATE_LPARAM</a> macro.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-get_keystate_lparam">GET_KEYSTATE_LPARAM</a>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Reference</b>
