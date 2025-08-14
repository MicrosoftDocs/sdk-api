---
UID: NF:winuser.MAKELRESULT
title: MAKELRESULT macro (winuser.h)
description: Creates a value for use as a return value from a window procedure. The macro concatenates the specified values.
helpviewer_keywords: ["MAKELRESULT","MAKELRESULT macro [Windows and Messages]","_win32_MAKELRESULT","_win32_makelresult_cpp","winmsg.makelresult","winui._win32_makelresult","winuser/MAKELRESULT"]
old-location: winmsg\makelresult.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmacros\makelresult.htm
ms.date: 07/01/2025
ms.keywords: MAKELRESULT, MAKELRESULT macro [Windows and Messages], _win32_MAKELRESULT, _win32_makelresult_cpp, winmsg.makelresult, winui._win32_makelresult, winuser/MAKELRESULT
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
 - MAKELRESULT
 - winuser/MAKELRESULT
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
 - MAKELRESULT
---

# MAKELRESULT macro

## -syntax

```cpp
LRESULT MAKELRESULT(
    WORD l,
    WORD h
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

The return value is an **LRESULT** value.


## -description

Creates a value for use as a return value from a window procedure. The macro concatenates the specified values.

## -parameters

### -param l

The low-order word of the new value.

### -param h

The high-order word of the new value.

## -see-also

<b>Conceptual</b>



<a href="/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)">MAKELONG</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makelparam">MAKELPARAM</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makewparam">MAKEWPARAM</a>



<b>Reference</b>



<a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>
