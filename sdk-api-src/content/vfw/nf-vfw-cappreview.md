---
UID: NF:vfw.capPreview
title: capPreview macro (vfw.h)
description: The capPreview macro enables or disables preview mode.
helpviewer_keywords: ["_win32_capPreview","capPreview","capPreview macro [Windows Multimedia]","multimedia.cappreview","vfw/capPreview"]
old-location: multimedia\cappreview.htm
tech.root: Multimedia
ms.assetid: c6888e35-9915-4ffb-ac0d-3cc1419fdac3
ms.date: 07/01/2025
ms.keywords: _win32_capPreview, capPreview, capPreview macro [Windows Multimedia], multimedia.cappreview, vfw/capPreview
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
 - capPreview
 - vfw/capPreview
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
 - capPreview
---

# capPreview macro

## -syntax

```cpp
BOOL capPreview(
     hwnd,
     f
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capPreview</b> macro enables or disables preview mode. In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-preview">WM_CAP_SET_PREVIEW</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param f

Preview flag. Specify <b>TRUE</b> for this parameter to enable preview mode or <b>FALSE</b> to disable it.

## -remarks

The preview mode uses substantial CPU resources. Applications can disable preview or lower the preview rate when another application has the focus. The <b>fLiveWindow</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-capstatus">CAPSTATUS</a> structure indicates if preview mode is currently enabled.

Enabling preview mode automatically disables overlay mode.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
