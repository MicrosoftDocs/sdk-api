---
UID: NF:vfw.MCIWndSetPalette
title: MCIWndSetPalette macro (vfw.h)
description: The MCIWndSetPalette macro sends a palette handle to the MCI device associated with the MCIWnd window. You can use this macro or explicitly send the MCIWNDM_SETPALETTE message.
helpviewer_keywords: ["MCIWndSetPalette","MCIWndSetPalette macro [Windows Multimedia]","_win32_MCIWndSetPalette","multimedia.mciwndsetpalette","vfw/MCIWndSetPalette"]
old-location: multimedia\mciwndsetpalette.htm
tech.root: Multimedia
ms.assetid: dba9370b-2412-47b2-a140-bc787a448024
ms.date: 07/01/2025
ms.keywords: MCIWndSetPalette, MCIWndSetPalette macro [Windows Multimedia], _win32_MCIWndSetPalette, multimedia.mciwndsetpalette, vfw/MCIWndSetPalette
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
 - MCIWndSetPalette
 - vfw/MCIWndSetPalette
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
 - MCIWndSetPalette
---

# MCIWndSetPalette macro

## -syntax

```cpp
LONG MCIWndSetPalette(
     hwnd,
     hpal
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndSetPalette</b> macro sends a palette handle to the MCI device associated with the MCIWnd window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-setpalette">MCIWNDM_SETPALETTE</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param hpal

Palette handle.
