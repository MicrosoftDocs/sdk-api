---
UID: NF:vfw.MCIWndCanWindow
title: MCIWndCanWindow macro (vfw.h)
description: The MCIWndCanWindow macro determines if an MCI device supports window-oriented MCI commands. You can use this macro or explicitly send the MCIWNDM_CAN_WINDOW message.
helpviewer_keywords: ["MCIWndCanWindow","MCIWndCanWindow macro [Windows Multimedia]","_win32_MCIWndCanWindow","multimedia.mciwndcanwindow","vfw/MCIWndCanWindow"]
old-location: multimedia\mciwndcanwindow.htm
tech.root: Multimedia
ms.assetid: 2db1d83a-3e03-474e-b36e-8b3b3e3faa82
ms.date: 07/01/2025
ms.keywords: MCIWndCanWindow, MCIWndCanWindow macro [Windows Multimedia], _win32_MCIWndCanWindow, multimedia.mciwndcanwindow, vfw/MCIWndCanWindow
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
 - MCIWndCanWindow
 - vfw/MCIWndCanWindow
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
 - MCIWndCanWindow
---

# MCIWndCanWindow macro

## -syntax

```cpp
BOOL MCIWndCanWindow(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.


## -description

The <b>MCIWndCanWindow</b> macro determines if an MCI device supports window-oriented MCI commands. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-can-window">MCIWNDM_CAN_WINDOW</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-can-window">MCIWNDM_CAN_WINDOW</a>
