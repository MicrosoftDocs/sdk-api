---
UID: NF:vfw.MCIWndGetPalette
title: MCIWndGetPalette macro (vfw.h)
description: The MCIWndGetPalette macro retrieves a handle of the palette used by an MCI device. You can use this macro or explicitly send the MCIWNDM_GETPALETTE message.
helpviewer_keywords: ["MCIWndGetPalette","MCIWndGetPalette macro [Windows Multimedia]","_win32_MCIWndGetPalette","multimedia.mciwndgetpalette","vfw/MCIWndGetPalette"]
old-location: multimedia\mciwndgetpalette.htm
tech.root: Multimedia
ms.assetid: cb42fdcc-35c0-4099-97bf-a3c8c1e53047
ms.date: 07/01/2025
ms.keywords: MCIWndGetPalette, MCIWndGetPalette macro [Windows Multimedia], _win32_MCIWndGetPalette, multimedia.mciwndgetpalette, vfw/MCIWndGetPalette
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
 - MCIWndGetPalette
 - vfw/MCIWndGetPalette
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
 - MCIWndGetPalette
---

# MCIWndGetPalette macro

## -syntax

```cpp
HPALETTE MCIWndGetPalette(
     hwnd
);
```

## -returns

Type: **HPALETTE**

Returns the handle of the palette if successful.


## -description

The <b>MCIWndGetPalette</b> macro retrieves a handle of the palette used by an MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getpalette">MCIWNDM_GETPALETTE</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getpalette">MCIWNDM_GETPALETTE</a>



<a href="/windows/desktop/api/vfw/nf-vfw-mciwndgetpalette">MCIWndGetPalette</a>
