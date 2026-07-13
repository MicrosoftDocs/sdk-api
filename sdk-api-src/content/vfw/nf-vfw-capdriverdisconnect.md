---
UID: NF:vfw.capDriverDisconnect
title: capDriverDisconnect macro (vfw.h)
description: The capDriverDisconnect macro disconnects a capture driver from a capture window. You can use this macro or explicitly send the WM_CAP_DRIVER_DISCONNECT message.
helpviewer_keywords: ["_win32_capDriverDisconnect","capDriverDisconnect","capDriverDisconnect macro [Windows Multimedia]","multimedia.capdriverdisconnect","vfw/capDriverDisconnect"]
old-location: multimedia\capdriverdisconnect.htm
tech.root: Multimedia
ms.assetid: c009adb4-bc73-4d0d-9ab1-801e92e8851f
ms.date: 07/01/2025
ms.keywords: _win32_capDriverDisconnect, capDriverDisconnect, capDriverDisconnect macro [Windows Multimedia], multimedia.capdriverdisconnect, vfw/capDriverDisconnect
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
 - capDriverDisconnect
 - vfw/capDriverDisconnect
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
 - capDriverDisconnect
---

# capDriverDisconnect macro

## -syntax

```cpp
BOOL capDriverDisconnect(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.


## -description

The <b>capDriverDisconnect</b> macro disconnects a capture driver from a capture window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-driver-disconnect">WM_CAP_DRIVER_DISCONNECT</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
