---
UID: NF:vfw.MCIWndGetStyles
title: MCIWndGetStyles macro (vfw.h)
description: The MCIWndGetStyles macro retrieves the flags specifying the current MCIWnd window styles used by a window. You can use this macro or explicitly send the MCIWNDM_GETSTYLES message.
helpviewer_keywords: ["MCIWndGetStyles","MCIWndGetStyles macro [Windows Multimedia]","_win32_MCIWndGetStyles","multimedia.mciwndgetstyles","vfw/MCIWndGetStyles"]
old-location: multimedia\mciwndgetstyles.htm
tech.root: Multimedia
ms.assetid: 06d022a7-7772-4442-b21c-4f18e9eedbc3
ms.date: 07/01/2025
ms.keywords: MCIWndGetStyles, MCIWndGetStyles macro [Windows Multimedia], _win32_MCIWndGetStyles, multimedia.mciwndgetstyles, vfw/MCIWndGetStyles
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
 - MCIWndGetStyles
 - vfw/MCIWndGetStyles
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
 - MCIWndGetStyles
---

# MCIWndGetStyles macro

## -syntax

```cpp
UINT MCIWndGetStyles(
     hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns a value representing the current styles of the MCIWnd window. The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).


## -description

The <b>MCIWndGetStyles</b> macro retrieves the flags specifying the current MCIWnd window styles used by a window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getstyles">MCIWNDM_GETSTYLES</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getstyles">MCIWNDM_GETSTYLES</a>
