---
UID: NF:winuser.GET_WHEEL_DELTA_WPARAM
title: GET_WHEEL_DELTA_WPARAM macro (winuser.h)
description: Retrieves the wheel-delta value from the specified WPARAM value.
helpviewer_keywords: ["GET_WHEEL_DELTA_WPARAM","GET_WHEEL_DELTA_WPARAM macro [Keyboard and Mouse Input]","_win32_GET_WHEEL_DELTA_WPARAM","_win32_get_wheel_delta_wparam_cpp","inputdev.get_wheel_delta_wparam","winui._win32_get_wheel_delta_wparam","winuser/GET_WHEEL_DELTA_WPARAM"]
old-location: inputdev\get_wheel_delta_wparam.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputmacros\get_wheel_delta_wparam.htm
ms.date: 07/01/2025
ms.keywords: GET_WHEEL_DELTA_WPARAM, GET_WHEEL_DELTA_WPARAM macro [Keyboard and Mouse Input], _win32_GET_WHEEL_DELTA_WPARAM, _win32_get_wheel_delta_wparam_cpp, inputdev.get_wheel_delta_wparam, winui._win32_get_wheel_delta_wparam, winuser/GET_WHEEL_DELTA_WPARAM
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
 - GET_WHEEL_DELTA_WPARAM
 - winuser/GET_WHEEL_DELTA_WPARAM
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
 - GET_WHEEL_DELTA_WPARAM
---

# GET_WHEEL_DELTA_WPARAM macro

## -syntax

```cpp
short GET_WHEEL_DELTA_WPARAM(
    WPARAM wParam
);
```

## -returns

Type: **short**

The return value is the high-order word representing the wheel-delta value. It indicates the distance that the wheel is rotated, expressed in multiples or divisions of WHEEL_DELTA, which is 120. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.


## -description

Retrieves the wheel-delta value from the specified <b>WPARAM</b> value.

## -parameters

### -param wParam

The value to be converted.

## -see-also

<a href="/windows/desktop/inputdev/mouse-input">Mouse Input Overview</a>
