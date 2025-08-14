---
UID: NF:vfw.MCIWndCanEject
title: MCIWndCanEject macro (vfw.h)
description: The MCIWndCanEject macro determines if an MCI device can eject its media. You can use this macro or explicitly send the MCIWNDM_CAN_EJECT message.
helpviewer_keywords: ["MCIWndCanEject","MCIWndCanEject macro [Windows Multimedia]","_win32_MCIWndCanEject","multimedia.mciwndcaneject","vfw/MCIWndCanEject"]
old-location: multimedia\mciwndcaneject.htm
tech.root: Multimedia
ms.assetid: de5021d2-9e96-4fe4-99c7-91ffb2b11c7f
ms.date: 07/01/2025
ms.keywords: MCIWndCanEject, MCIWndCanEject macro [Windows Multimedia], _win32_MCIWndCanEject, multimedia.mciwndcaneject, vfw/MCIWndCanEject
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
 - MCIWndCanEject
 - vfw/MCIWndCanEject
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
 - MCIWndCanEject
---

# MCIWndCanEject macro

## -syntax

```cpp
BOOL MCIWndCanEject(
    HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the device can eject its media or **FALSE** otherwise.

## -description

The <b>MCIWndCanEject</b> macro determines if an MCI device can eject its media. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-can-eject">MCIWNDM_CAN_EJECT</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-can-eject">MCIWNDM_CAN_EJECT</a>
