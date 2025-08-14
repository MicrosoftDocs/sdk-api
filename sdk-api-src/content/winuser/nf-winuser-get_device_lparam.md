---
UID: NF:winuser.GET_DEVICE_LPARAM
title: GET_DEVICE_LPARAM macro (winuser.h)
description: Retrieves the input device type from the specified LPARAM value.
helpviewer_keywords: ["GET_DEVICE_LPARAM","GET_DEVICE_LPARAM macro [Keyboard and Mouse Input]","_win32_GET_DEVICE_LPARAM","_win32_get_device_lparam_cpp","inputdev.get_device_lparam","winui._win32_get_device_lparam","winuser/GET_DEVICE_LPARAM"]
tech.root: inputdev
ms.date: 07/01/2025
ms.keywords: GET_DEVICE_LPARAM, GET_DEVICE_LPARAM macro [Keyboard and Mouse Input], _win32_GET_DEVICE_LPARAM, _win32_get_device_lparam_cpp, inputdev.get_device_lparam, winui._win32_get_device_lparam, winuser/GET_DEVICE_LPARAM
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
 - GET_DEVICE_LPARAM
 - winuser/GET_DEVICE_LPARAM
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
 - GET_DEVICE_LPARAM
---

# GET_DEVICE_LPARAM macro

## -syntax

```cpp
WORD GET_DEVICE_LPARAM(
    LPARAM lParam
);
```

## -description

Retrieves the input device type from the specified **LPARAM** value.

## -parameters

### -param lParam

The value to be converted.

## -returns

Type: **WORD**

The return value is the bit of the high-order word representing the input device type. It can be one of the following values.

| Return code | Value | Description |
|--|--|--|
| **FAPPCOMMAND_KEY** | 0 | User pressed a key. |
| **FAPPCOMMAND_MOUSE** | 0x8000 | User clicked a mouse button. |
| **FAPPCOMMAND_OEM** | 0x1000 | An unidentified hardware source generated the event. It could be a mouse or a keyboard event. |

## -remarks

This macro is identical to the [GET_MOUSEORKEY_LPARAM macro](/windows/win32/winmsg/nf-winuser-get_mouseorkey_lparam).

## -see-also

[GET_MOUSEORKEY_LPARAM macro](/windows/win32/winmsg/nf-winuser-get_mouseorkey_lparam), [Mouse Input](/windows/win32/inputdev/mouse-input)
