---
UID: NF:vfw.MCIWndGetInactiveTimer
title: MCIWndGetInactiveTimer macro (vfw.h)
description: The MCIWndGetInactiveTimer macro retrieves the update period used when the MCIWnd window is the inactive window. You can use this macro or explicitly send the MCIWNDM_GETINACTIVETIMER message.
helpviewer_keywords: ["MCIWndGetInactiveTimer","MCIWndGetInactiveTimer macro [Windows Multimedia]","_win32_MCIWndGetInactiveTimer","multimedia.mciwndgetinactivetimer","vfw/MCIWndGetInactiveTimer"]
old-location: multimedia\mciwndgetinactivetimer.htm
tech.root: Multimedia
ms.assetid: a9683a34-7fbd-4878-a547-4421d5888308
ms.date: 07/01/2025
ms.keywords: MCIWndGetInactiveTimer, MCIWndGetInactiveTimer macro [Windows Multimedia], _win32_MCIWndGetInactiveTimer, multimedia.mciwndgetinactivetimer, vfw/MCIWndGetInactiveTimer
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
 - MCIWndGetInactiveTimer
 - vfw/MCIWndGetInactiveTimer
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
 - MCIWndGetInactiveTimer
---

# MCIWndGetInactiveTimer macro

## -syntax

```cpp
UINT MCIWndGetInactiveTimer(
     hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the update period, in milliseconds. The default value is 2000 milliseconds.


## -description

The <b>MCIWndGetInactiveTimer</b> macro retrieves the update period used when the MCIWnd window is the inactive window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getinactivetimer">MCIWNDM_GETINACTIVETIMER</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getinactivetimer">MCIWNDM_GETINACTIVETIMER</a>
