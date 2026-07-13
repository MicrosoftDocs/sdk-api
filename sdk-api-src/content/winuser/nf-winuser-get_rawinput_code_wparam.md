---
UID: NF:winuser.GET_RAWINPUT_CODE_WPARAM
title: GET_RAWINPUT_CODE_WPARAM macro (winuser.h)
description: Retrieves the input code from wParam in WM_INPUT.
helpviewer_keywords: ["GET_RAWINPUT_CODE_WPARAM","GET_RAWINPUT_CODE_WPARAM macro [Keyboard and Mouse Input]","RIM_INPUT","RIM_INPUTSINK","_win32_GET_RAWINPUT_CODE_WPARAM","_win32_get_rawinput_code_wparam_cpp","inputdev.get_rawinput_code_wparam","winui._win32_get_rawinput_code_wparam","winuser/GET_RAWINPUT_CODE_WPARAM"]
old-location: inputdev\get_rawinput_code_wparam.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputmacros\get_rawinput_code_wparam.htm
ms.date: 07/01/2025
ms.keywords: GET_RAWINPUT_CODE_WPARAM, GET_RAWINPUT_CODE_WPARAM macro [Keyboard and Mouse Input], RIM_INPUT, RIM_INPUTSINK, _win32_GET_RAWINPUT_CODE_WPARAM, _win32_get_rawinput_code_wparam_cpp, inputdev.get_rawinput_code_wparam, winui._win32_get_rawinput_code_wparam, winuser/GET_RAWINPUT_CODE_WPARAM
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - GET_RAWINPUT_CODE_WPARAM
 - winuser/GET_RAWINPUT_CODE_WPARAM
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
 - GET_RAWINPUT_CODE_WPARAM
---

# GET_RAWINPUT_CODE_WPARAM macro

## -syntax

```cpp
WPARAM GET_RAWINPUT_CODE_WPARAM(
    WPARAM wParam
);
```


## -description

Retrieves the input code from <i>wParam</i> in [WM_INPUT](/windows/desktop/inputdev/wm-input) message.

## -parameters

### -param wParam

<i>wParam</i> from [WM_INPUT](/windows/desktop/inputdev/wm-input) message.

## -returns

Input code value. Can be one of the following:

| Value                | Meaning                                                         |
| -------------------- | --------------------------------------------------------------- |
| **RIM\_INPUT** 0     | Input occurred while the application was in the foreground.     |
| **RIM\_INPUTSINK** 1 | Input occurred while the application was not in the foreground. |

## -see-also

**Conceptual**

[RAWINPUT](ns-winuser-rawinput.md)

[Raw Input](/windows/desktop/inputdev/raw-input)

**Reference**

[WM_INPUT](/windows/desktop/inputdev/wm-input)
