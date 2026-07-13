---
UID: NF:winuser.GET_APPCOMMAND_LPARAM
title: GET_APPCOMMAND_LPARAM macro (winuser.h)
description: Retrieves the application command from the specified LPARAM value.
helpviewer_keywords: ["GET_APPCOMMAND_LPARAM","GET_APPCOMMAND_LPARAM macro [Keyboard and Mouse Input]","_win32_GET_APPCOMMAND_LPARAM","_win32_get_appcommand_lparam_cpp","inputdev.get_appcommand_lparam","winui._win32_get_appcommand_lparam","winuser/GET_APPCOMMAND_LPARAM"]
old-location: inputdev\get_appcommand_lparam.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputmacros\get_appcommand_lparam.htm
ms.date: 07/01/2025
ms.keywords: GET_APPCOMMAND_LPARAM, GET_APPCOMMAND_LPARAM macro [Keyboard and Mouse Input], _win32_GET_APPCOMMAND_LPARAM, _win32_get_appcommand_lparam_cpp, inputdev.get_appcommand_lparam, winui._win32_get_appcommand_lparam, winuser/GET_APPCOMMAND_LPARAM
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
 - GET_APPCOMMAND_LPARAM
 - winuser/GET_APPCOMMAND_LPARAM
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
 - GET_APPCOMMAND_LPARAM
---

# GET_APPCOMMAND_LPARAM macro

## -syntax

```cpp
short GET_APPCOMMAND_LPARAM(
    LPARAM lParam
);
```

## -returns

Type: **short**

The return value is the bits of the high-order word representing the application command. It can be one of the following values.


## -description

Retrieves the application command from the specified <b>LPARAM</b> value.

## -parameters

### -param lParam

The value to be converted.

## -see-also

<a href="/windows/desktop/inputdev/mouse-input">Mouse Input Overview</a>
