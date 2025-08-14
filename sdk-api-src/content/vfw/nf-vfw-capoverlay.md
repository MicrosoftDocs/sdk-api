---
UID: NF:vfw.capOverlay
title: capOverlay macro (vfw.h)
description: The capOverlay macro enables or disables overlay mode. In overlay mode, video is displayed using hardware overlay. You can use this macro or explicitly call the WM_CAP_SET_OVERLAY message.
helpviewer_keywords: ["_win32_capOverlay","capOverlay","capOverlay macro [Windows Multimedia]","multimedia.capoverlay","vfw/capOverlay"]
old-location: multimedia\capoverlay.htm
tech.root: Multimedia
ms.assetid: a6508e33-7864-4f19-a844-0ba280028f43
ms.date: 07/01/2025
ms.keywords: _win32_capOverlay, capOverlay, capOverlay macro [Windows Multimedia], multimedia.capoverlay, vfw/capOverlay
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
 - capOverlay
 - vfw/capOverlay
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
 - capOverlay
---

# capOverlay macro

## -syntax

```cpp
BOOL capOverlay(
     hwnd,
     f
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capOverlay</b> macro enables or disables overlay mode. In overlay mode, video is displayed using hardware overlay. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-overlay">WM_CAP_SET_OVERLAY</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param f

Overlay flag. Specify <b>TRUE</b> for this parameter to enable overlay mode or <b>FALSE</b> to disable it.

## -remarks

Using an overlay does not require CPU resources.

The <b>fHasOverlay</b> member of the <b>CAPDRIVERCAPS</b> structure indicates whether the device is capable of overlay. The <b>fOverlayWindow</b> member of the <b>CAPSTATUS</b> structure indicates whether overlay mode is currently enabled.

Enabling overlay mode automatically disables preview mode.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
