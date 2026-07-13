---
UID: NF:vfw.MCIWndCanConfig
title: MCIWndCanConfig macro (vfw.h)
description: The MCIWndCanConfig macro determines if an MCI device can display a configuration dialog box. You can use this macro or explicitly send the MCIWNDM_CAN_CONFIG message.
helpviewer_keywords: ["MCIWndCanConfig","MCIWndCanConfig macro [Windows Multimedia]","_win32_MCIWndCanConfig","multimedia.mciwndcanconfig","vfw/MCIWndCanConfig"]
old-location: multimedia\mciwndcanconfig.htm
tech.root: Multimedia
ms.assetid: 63d3721a-41e6-46cd-a95a-ac3a82a422f7
ms.date: 07/01/2025
ms.keywords: MCIWndCanConfig, MCIWndCanConfig macro [Windows Multimedia], _win32_MCIWndCanConfig, multimedia.mciwndcanconfig, vfw/MCIWndCanConfig
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
 - MCIWndCanConfig
 - vfw/MCIWndCanConfig
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
 - MCIWndCanConfig
---

# MCIWndCanConfig macro

## -syntax

```cpp
BOOL MCIWndCanConfig(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the device supports configuration or **FALSE** otherwise.


## -description

The <b>MCIWndCanConfig</b> macro determines if an MCI device can display a configuration dialog box. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-can-config">MCIWNDM_CAN_CONFIG</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-can-config">MCIWNDM_CAN_CONFIG</a>
