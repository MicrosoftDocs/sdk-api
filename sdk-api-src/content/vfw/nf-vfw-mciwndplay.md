---
UID: NF:vfw.MCIWndPlay
title: MCIWndPlay macro (vfw.h)
description: The MCIWndPlay macro sends a command to an MCI device to start playing from the current position in the content. You can use this macro or explicitly send the MCI_PLAY command.
helpviewer_keywords: ["MCIWndPlay","MCIWndPlay macro [Windows Multimedia]","_win32_MCIWndPlay","multimedia.mciwndplay","vfw/MCIWndPlay"]
old-location: multimedia\mciwndplay.htm
tech.root: Multimedia
ms.assetid: bfa88925-2f2a-4bbb-bd89-479515f759ac
ms.date: 07/01/2025
ms.keywords: MCIWndPlay, MCIWndPlay macro [Windows Multimedia], _win32_MCIWndPlay, multimedia.mciwndplay, vfw/MCIWndPlay
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
 - MCIWndPlay
 - vfw/MCIWndPlay
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
 - MCIWndPlay
---

# MCIWndPlay macro

## -syntax

```cpp
LONG MCIWndPlay(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndPlay</b> macro sends a command to an MCI device to start playing from the current position in the content. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-play">MCI_PLAY</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.
