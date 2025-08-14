---
UID: NF:vfw.capPreviewScale
title: capPreviewScale macro (vfw.h)
description: The capPreviewScale macro enables or disables scaling of the preview video images.
helpviewer_keywords: ["_win32_capPreviewScale","capPreviewScale","capPreviewScale macro [Windows Multimedia]","multimedia.cappreviewscale","vfw/capPreviewScale"]
old-location: multimedia\cappreviewscale.htm
tech.root: Multimedia
ms.assetid: 32f432a7-76be-4b75-8863-bc67cdcda781
ms.date: 07/01/2025
ms.keywords: _win32_capPreviewScale, capPreviewScale, capPreviewScale macro [Windows Multimedia], multimedia.cappreviewscale, vfw/capPreviewScale
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
 - capPreviewScale
 - vfw/capPreviewScale
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
 - capPreviewScale
---

# capPreviewScale macro

## -syntax

```cpp
BOOL capPreviewScale(
     hwnd,
     f
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capPreviewScale</b> macro enables or disables scaling of the preview video images. If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-scale">WM_CAP_SET_SCALE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param f

Preview scaling flag. Specify <b>TRUE</b> for this parameter to stretch preview frames to the size of the capture window or <b>FALSE</b> to display them at their natural size.

## -remarks

Scaling preview images controls the immediate presentation of captured frames within the capture window. It has no effect on the size of the frames saved to file.

Scaling has no effect when using overlay to display video in the frame buffer.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
