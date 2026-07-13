---
UID: NF:vfw.MCIWndGetError
title: MCIWndGetError macro (vfw.h)
description: The MCIWndGetError macro retrieves the last MCI error encountered. You can use this macro or explicitly send the MCIWNDM_GETERROR message.
helpviewer_keywords: ["MCIWndGetError","MCIWndGetError macro [Windows Multimedia]","_win32_MCIWndGetError","multimedia.mciwndgeterror","vfw/MCIWndGetError"]
old-location: multimedia\mciwndgeterror.htm
tech.root: Multimedia
ms.assetid: 67cbd522-2409-4eeb-b62b-d78f8caea349
ms.date: 07/01/2025
ms.keywords: MCIWndGetError, MCIWndGetError macro [Windows Multimedia], _win32_MCIWndGetError, multimedia.mciwndgeterror, vfw/MCIWndGetError
req.header: vfw.h
req.include-header: 
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
 - MCIWndGetError
 - vfw/MCIWndGetError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndGetError
---

# MCIWndGetError macro

## -syntax

```cpp
LONG MCIWndGetError(
     hwnd,
     lp,
     len
);
```

## -returns

Type: **LONG**

Returns the integer error value if successful.


## -description

The <b>MCIWndGetError</b> macro retrieves the last MCI error encountered. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-geterror">MCIWNDM_GETERROR</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param lp

Pointer to an application-defined buffer used to return the error string.

### -param len

Size, in bytes, of the error buffer.

## -remarks

If <i>lp</i> is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer. If the error string is longer than the buffer, MCIWnd truncates it.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-geterror">MCIWNDM_GETERROR</a>
