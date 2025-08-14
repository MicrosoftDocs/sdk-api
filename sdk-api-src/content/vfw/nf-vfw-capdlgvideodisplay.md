---
UID: NF:vfw.capDlgVideoDisplay
title: capDlgVideoDisplay macro (vfw.h)
description: The capDlgVideoDisplay macro displays a dialog box in which the user can set or adjust the video output.
helpviewer_keywords: ["_win32_capDlgVideoDisplay","capDlgVideoDisplay","capDlgVideoDisplay macro [Windows Multimedia]","multimedia.capdlgvideodisplay","vfw/capDlgVideoDisplay"]
old-location: multimedia\capdlgvideodisplay.htm
tech.root: Multimedia
ms.assetid: 3feb6964-b897-4d5b-8861-7fca829e25e4
ms.date: 07/01/2025
ms.keywords: _win32_capDlgVideoDisplay, capDlgVideoDisplay, capDlgVideoDisplay macro [Windows Multimedia], multimedia.capdlgvideodisplay, vfw/capDlgVideoDisplay
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
 - capDlgVideoDisplay
 - vfw/capDlgVideoDisplay
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
 - capDlgVideoDisplay
---

# capDlgVideoDisplay macro

## -syntax

```cpp
BOOL capDlgVideoDisplay(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capDlgVideoDisplay</b> macro displays a dialog box in which the user can set or adjust the video output. This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-dlg-videodisplay">WM_CAP_DLG_VIDEODISPLAY</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.

The Video Display dialog box is unique for each capture driver. Some capture drivers might not support a Video Display dialog box. Applications can determine if the capture driver supports this message by checking the <b>fHasDlgVideoDisplay</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-capdrivercaps">CAPDRIVERCAPS</a> structure.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
