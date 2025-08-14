---
UID: NF:vfw.MCIWndGetActiveTimer
title: MCIWndGetActiveTimer macro (vfw.h)
description: The MCIWndGetActiveTimer macro retrieves the update period used when the MCIWnd window is the active window. You can use this macro or explicitly send the MCIWNDM_GETACTIVETIMER message.
helpviewer_keywords: ["MCIWndGetActiveTimer","MCIWndGetActiveTimer macro [Windows Multimedia]","_win32_MCIWndGetActiveTimer","multimedia.mciwndgetactivetimer","vfw/MCIWndGetActiveTimer"]
old-location: multimedia\mciwndgetactivetimer.htm
tech.root: Multimedia
ms.assetid: 581b9bb3-9bc0-46f2-a5d2-93397900ff28
ms.date: 07/01/2025
ms.keywords: MCIWndGetActiveTimer, MCIWndGetActiveTimer macro [Windows Multimedia], _win32_MCIWndGetActiveTimer, multimedia.mciwndgetactivetimer, vfw/MCIWndGetActiveTimer
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
 - MCIWndGetActiveTimer
 - vfw/MCIWndGetActiveTimer
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
 - MCIWndGetActiveTimer
---

# MCIWndGetActiveTimer macro

## -syntax

```cpp
UINT MCIWndGetActiveTimer(
     hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the update period in milliseconds. The default is 500 milliseconds.


## -description

The <b>MCIWndGetActiveTimer</b> macro retrieves the update period used when the MCIWnd window is the active window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getactivetimer">MCIWNDM_GETACTIVETIMER</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getactivetimer">MCIWNDM_GETACTIVETIMER</a>
