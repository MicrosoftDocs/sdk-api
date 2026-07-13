---
UID: NF:vfw.MCIWndUseFrames
title: MCIWndUseFrames macro (vfw.h)
description: The MCIWndUseFrames macro sets the time format of an MCI device to frames. You can use this macro or explicitly send the MCIWNDM_SETTIMEFORMAT message.
helpviewer_keywords: ["MCIWndUseFrames","MCIWndUseFrames macro [Windows Multimedia]","_win32_MCIWndUseFrames","multimedia.mciwnduseframes","vfw/MCIWndUseFrames"]
old-location: multimedia\mciwnduseframes.htm
tech.root: Multimedia
ms.assetid: 14c2ac12-6034-43f0-ac3e-ea3c6a01e39a
ms.date: 07/01/2025
ms.keywords: MCIWndUseFrames, MCIWndUseFrames macro [Windows Multimedia], _win32_MCIWndUseFrames, multimedia.mciwnduseframes, vfw/MCIWndUseFrames
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
 - MCIWndUseFrames
 - vfw/MCIWndUseFrames
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
 - MCIWndUseFrames
---

# MCIWndUseFrames macro

## -syntax

```cpp
LONG MCIWndUseFrames(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndUseFrames</b> macro sets the time format of an MCI device to frames. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-settimeformat">MCIWNDM_SETTIMEFORMAT</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.
