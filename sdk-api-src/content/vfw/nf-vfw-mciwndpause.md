---
UID: NF:vfw.MCIWndPause
title: MCIWndPause macro (vfw.h)
description: The MCIWndPause macro sends a command to an MCI device to pause playing or recording.
helpviewer_keywords: ["MCIWndPause","MCIWndPause macro [Windows Multimedia]","_win32_MCIWndPause","multimedia.mciwndpause","vfw/MCIWndPause"]
old-location: multimedia\mciwndpause.htm
tech.root: Multimedia
ms.assetid: 3c5e0209-f64b-4235-9855-e5ad4ce88032
ms.date: 07/01/2025
ms.keywords: MCIWndPause, MCIWndPause macro [Windows Multimedia], _win32_MCIWndPause, multimedia.mciwndpause, vfw/MCIWndPause
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
 - MCIWndPause
 - vfw/MCIWndPause
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
 - MCIWndPause
---

# MCIWndPause macro

## -syntax

```cpp
LONG MCIWndPause(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndPause</b> macro sends a command to an MCI device to pause playing or recording.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

