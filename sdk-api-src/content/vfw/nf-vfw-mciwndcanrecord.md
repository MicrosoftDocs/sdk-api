---
UID: NF:vfw.MCIWndCanRecord
title: MCIWndCanRecord macro (vfw.h)
description: The MCIWndCanRecord macro determines if an MCI device supports recording. You can use this macro or explicitly send the MCIWNDM_CAN_RECORD message.
helpviewer_keywords: ["MCIWndCanRecord","MCIWndCanRecord macro [Windows Multimedia]","_win32_MCIWndCanRecord","multimedia.mciwndcanrecord","vfw/MCIWndCanRecord"]
old-location: multimedia\mciwndcanrecord.htm
tech.root: Multimedia
ms.assetid: 836747de-9306-4219-b462-e2c8efd42666
ms.date: 07/01/2025
ms.keywords: MCIWndCanRecord, MCIWndCanRecord macro [Windows Multimedia], _win32_MCIWndCanRecord, multimedia.mciwndcanrecord, vfw/MCIWndCanRecord
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
 - MCIWndCanRecord
 - vfw/MCIWndCanRecord
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
 - MCIWndCanRecord
---

# MCIWndCanRecord macro

## -syntax

```cpp
BOOL MCIWndCanRecord(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the device supports recording or **FALSE** otherwise.


## -description

The <b>MCIWndCanRecord</b> macro determines if an MCI device supports recording. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-can-record">MCIWNDM_CAN_RECORD</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-can-record">MCIWNDM_CAN_RECORD</a>
