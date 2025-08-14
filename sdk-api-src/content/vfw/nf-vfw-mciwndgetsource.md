---
UID: NF:vfw.MCIWndGetSource
title: MCIWndGetSource macro (vfw.h)
description: The MCIWndGetSource macro retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback. You can use this macro or explicitly send the MCIWNDM_GET_SOURCE message.
helpviewer_keywords: ["MCIWndGetSource","MCIWndGetSource macro [Windows Multimedia]","_win32_MCIWndGetSource","multimedia.mciwndgetsource","vfw/MCIWndGetSource"]
old-location: multimedia\mciwndgetsource.htm
tech.root: Multimedia
ms.assetid: 3ac01055-7d17-499f-af2e-e50fc08e5520
ms.date: 07/01/2025
ms.keywords: MCIWndGetSource, MCIWndGetSource macro [Windows Multimedia], _win32_MCIWndGetSource, multimedia.mciwndgetsource, vfw/MCIWndGetSource
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
 - MCIWndGetSource
 - vfw/MCIWndGetSource
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
 - MCIWndGetSource
---

# MCIWndGetSource macro

## -syntax

```cpp
LONG MCIWndGetSource(
     hwnd,
     prc
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndGetSource</b> macro retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-get-source">MCIWNDM_GET_SOURCE</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param prc

Pointer to a RECT structure to contain the coordinates of the source rectangle.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-get-source">MCIWNDM_GET_SOURCE</a>
