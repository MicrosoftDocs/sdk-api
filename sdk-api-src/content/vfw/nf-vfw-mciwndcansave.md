---
UID: NF:vfw.MCIWndCanSave
title: MCIWndCanSave macro (vfw.h)
description: The MCIWndCanSave macro determines if an MCI device can save data. You can use this macro or explicitly send the MCIWNDM_CAN_SAVE message.
helpviewer_keywords: ["MCIWndCanSave","MCIWndCanSave macro [Windows Multimedia]","_win32_MCIWndCanSave","multimedia.mciwndcansave","vfw/MCIWndCanSave"]
old-location: multimedia\mciwndcansave.htm
tech.root: Multimedia
ms.assetid: dc08b385-3e19-480d-ab05-58fd9b8c6b3a
ms.date: 07/01/2025
ms.keywords: MCIWndCanSave, MCIWndCanSave macro [Windows Multimedia], _win32_MCIWndCanSave, multimedia.mciwndcansave, vfw/MCIWndCanSave
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
 - MCIWndCanSave
 - vfw/MCIWndCanSave
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
 - MCIWndCanSave
---

# MCIWndCanSave macro

## -syntax

```cpp
BOOL MCIWndCanSave(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the device supports saving data or **FALSE** otherwise.


## -description

The <b>MCIWndCanSave</b> macro determines if an MCI device can save data. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-can-save">MCIWNDM_CAN_SAVE</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-can-save">MCIWNDM_CAN_SAVE</a>
