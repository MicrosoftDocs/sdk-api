---
UID: NF:vfw.MCIWndPutDest
title: MCIWndPutDest macro (vfw.h)
description: The MCIWndPutDest macro redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the MCIWNDM_PUT_DEST message.
helpviewer_keywords: ["MCIWndPutDest","MCIWndPutDest macro [Windows Multimedia]","_win32_MCIWndPutDest","multimedia.mciwndputdest","vfw/MCIWndPutDest"]
old-location: multimedia\mciwndputdest.htm
tech.root: Multimedia
ms.assetid: d058c1b7-f7f8-49a0-84cc-ece298a25289
ms.date: 07/01/2025
ms.keywords: MCIWndPutDest, MCIWndPutDest macro [Windows Multimedia], _win32_MCIWndPutDest, multimedia.mciwndputdest, vfw/MCIWndPutDest
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
 - MCIWndPutDest
 - vfw/MCIWndPutDest
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
 - MCIWndPutDest
---

# MCIWndPutDest macro

## -syntax

```cpp
LONG MCIWndPutDest(
     hwnd,
     prc
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndPutDest</b> macro redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-put-dest">MCIWNDM_PUT_DEST</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param prc

Pointer to a RECT structure containing the coordinates of the destination rectangle.
