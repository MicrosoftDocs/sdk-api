---
UID: NF:vfw.MCIWndEject
title: MCIWndEject macro (vfw.h)
description: The MCIWndEject macro sends a command to an MCI device to eject its media. You can use this macro or explicitly send the MCIWNDM_EJECT message.
helpviewer_keywords: ["MCIWndEject","MCIWndEject macro [Windows Multimedia]","_win32_MCIWndEject","multimedia.mciwndeject","vfw/MCIWndEject"]
old-location: multimedia\mciwndeject.htm
tech.root: Multimedia
ms.assetid: 7d86cc61-849d-40a3-9e8f-e319b0c9ea48
ms.date: 07/01/2025
ms.keywords: MCIWndEject, MCIWndEject macro [Windows Multimedia], _win32_MCIWndEject, multimedia.mciwndeject, vfw/MCIWndEject
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
 - MCIWndEject
 - vfw/MCIWndEject
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
 - MCIWndEject
---

# MCIWndEject macro

## -syntax

```cpp
LONG MCIWndEject(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndEject</b> macro sends a command to an MCI device to eject its media. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-eject">MCIWNDM_EJECT</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-eject">MCIWNDM_EJECT</a>
