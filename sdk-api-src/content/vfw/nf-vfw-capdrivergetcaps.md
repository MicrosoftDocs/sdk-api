---
UID: NF:vfw.capDriverGetCaps
title: capDriverGetCaps macro (vfw.h)
description: The capDriverGetCaps macro returns the hardware capabilities of the capture driver currently connected to a capture window. You can use this macro or explicitly send the WM_CAP_DRIVER_GET_CAPS message.
helpviewer_keywords: ["_win32_capDriverGetCaps","capDriverGetCaps","capDriverGetCaps macro [Windows Multimedia]","multimedia.capdrivergetcaps","vfw/capDriverGetCaps"]
old-location: multimedia\capdrivergetcaps.htm
tech.root: Multimedia
ms.assetid: 2ca3a1b1-1d88-480f-b079-82da111c4565
ms.date: 07/01/2025
ms.keywords: _win32_capDriverGetCaps, capDriverGetCaps, capDriverGetCaps macro [Windows Multimedia], multimedia.capdrivergetcaps, vfw/capDriverGetCaps
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
 - capDriverGetCaps
 - vfw/capDriverGetCaps
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
 - capDriverGetCaps
---

# capDriverGetCaps macro

## -syntax

```cpp
BOOL capDriverGetCaps(
     hwnd,
     s,
     wSize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.


## -description

The <b>capDriverGetCaps</b> macro returns the hardware capabilities of the capture driver currently connected to a capture window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-driver-get-caps">WM_CAP_DRIVER_GET_CAPS</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param s

Pointer to the <a href="/windows/desktop/api/vfw/ns-vfw-capdrivercaps">CAPDRIVERCAPS</a> structure to contain the hardware capabilities.

### -param wSize

Size, in bytes, of the structure referenced by <i>psCaps</i>.

## -remarks

The capabilities returned in <a href="/windows/desktop/api/vfw/ns-vfw-capdrivercaps">CAPDRIVERCAPS</a> are constant for a given capture driver. Applications need to retrieve this information once when the capture driver is first connected to a capture window.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
