---
UID: NF:winuser.GET_NCHITTEST_WPARAM
title: GET_NCHITTEST_WPARAM macro (winuser.h)
description: Retrieves the hit-test value from the specified WPARAM value.
helpviewer_keywords: ["GET_NCHITTEST_WPARAM","GET_NCHITTEST_WPARAM macro [Keyboard and Mouse Input]","_win32_GET_NCHITTEST_WPARAM","_win32_get_nchittest_wparam_cpp","inputdev.get_nchittest_wparam","winui._win32_get_nchittest_wparam","winuser/GET_NCHITTEST_WPARAM"]
old-location: inputdev\get_nchittest_wparam.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputmacros\get_nchittest_wparam.htm
ms.date: 07/01/2025
ms.keywords: GET_NCHITTEST_WPARAM, GET_NCHITTEST_WPARAM macro [Keyboard and Mouse Input], _win32_GET_NCHITTEST_WPARAM, _win32_get_nchittest_wparam_cpp, inputdev.get_nchittest_wparam, winui._win32_get_nchittest_wparam, winuser/GET_NCHITTEST_WPARAM
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
 - GET_NCHITTEST_WPARAM
 - winuser/GET_NCHITTEST_WPARAM
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
 - GET_NCHITTEST_WPARAM
---

# GET_NCHITTEST_WPARAM macro

## -syntax

```cpp
short GET_NCHITTEST_WPARAM(
    WPARAM wParam
);
```

## -returns

Type: **short**

The return value is the low-order word representing the hit-test value. For a list of hit-test values, see [WM_NCHITTEST](/windows/win32/inputdev/wm-nchittest).


## -description

Retrieves the hit-test value from the specified <b>WPARAM</b> value.

## -parameters

### -param wParam

The value to be converted.

## -see-also

<a href="/windows/desktop/inputdev/mouse-input">Mouse Input Overview</a>
