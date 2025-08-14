---
UID: NF:windowsx.GET_X_LPARAM
title: GET_X_LPARAM macro (windowsx.h)
description: Retrieves the signed x-coordinate from the specified LPARAM value.
helpviewer_keywords: ["GET_X_LPARAM","GET_X_LPARAM macro [Windows and Messages]","_win32_GET_X_LPARAM","_win32_get_x_lparam_cpp","windowsx/GET_X_LPARAM","winmsg.get_x_lparam","winui._win32_get_x_lparam"]
old-location: winmsg\get_x_lparam.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmacros\get_x_lparam.htm
ms.date: 07/01/2025
ms.keywords: GET_X_LPARAM, GET_X_LPARAM macro [Windows and Messages], _win32_GET_X_LPARAM, _win32_get_x_lparam_cpp, windowsx/GET_X_LPARAM, winmsg.get_x_lparam, winui._win32_get_x_lparam
req.header: windowsx.h
req.include-header: Windowsx.h
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
 - GET_X_LPARAM
 - windowsx/GET_X_LPARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - GET_X_LPARAM
---

# GET_X_LPARAM macro

## -syntax

```cpp
int GET_X_LPARAM(
    LPARAM lp
);
```

## -description

Retrieves the signed x-coordinate from the specified <b>LPARAM</b> value.

## -parameters

### -param lp

The data from which the x-coordinate is to be extracted.

## -returns

Type: <b>int</b>

X-coordinate.

## -remarks

Use <b>GET_X_LPARAM</b> instead of <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> to extract signed coordinate data. Negative screen coordinates may be returned on multiple monitor systems.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam">GET_Y_LPARAM</a>

<a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a>

<b>Reference</b>

<a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>
