---
UID: NF:winuser.GET_XBUTTON_WPARAM
title: GET_XBUTTON_WPARAM macro (winuser.h)
description: Retrieves the state of certain buttons from the specified WPARAM value.
helpviewer_keywords: ["GET_XBUTTON_WPARAM","GET_XBUTTON_WPARAM macro [Keyboard and Mouse Input]","_win32_GET_XBUTTON_WPARAM","_win32_get_xbutton_wparam_cpp","inputdev.get_xbutton_wparam","winui._win32_get_xbutton_wparam","winuser/GET_XBUTTON_WPARAM"]
old-location: inputdev\get_xbutton_wparam.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputmacros\get_xbutton_wparam.htm
ms.date: 07/01/2025
ms.keywords: GET_XBUTTON_WPARAM, GET_XBUTTON_WPARAM macro [Keyboard and Mouse Input], _win32_GET_XBUTTON_WPARAM, _win32_get_xbutton_wparam_cpp, inputdev.get_xbutton_wparam, winui._win32_get_xbutton_wparam, winuser/GET_XBUTTON_WPARAM
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
 - GET_XBUTTON_WPARAM
 - winuser/GET_XBUTTON_WPARAM
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
 - GET_XBUTTON_WPARAM
---

# GET_XBUTTON_WPARAM macro

## -syntax

```cpp
int GET_XBUTTON_WPARAM(
    WPARAM wParam
);
```

## -returns

Type: **int**

The high-order word indicates which button was released. It can be either of the following values:

| Return code | Value | Description |
|--|--|--|
| **XBUTTON1** | 0x0001 | The first X button was released. |
| **XBUTTON2** | 0x0002 | The second X button was released. |


## -description

Retrieves the state of certain buttons from the specified <b>WPARAM</b> value.

## -parameters

### -param wParam

The value to be converted.

## -see-also

<a href="/windows/desktop/inputdev/mouse-input">Mouse Input Overview</a>
