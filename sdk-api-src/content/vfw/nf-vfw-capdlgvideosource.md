---
UID: NF:vfw.capDlgVideoSource
title: capDlgVideoSource macro (vfw.h)
description: The capDlgVideoSource macro displays a dialog box in which the user can control the video source.
helpviewer_keywords: ["_win32_capDlgVideoSource","capDlgVideoSource","capDlgVideoSource macro [Windows Multimedia]","multimedia.capdlgvideosource","vfw/capDlgVideoSource"]
old-location: multimedia\capdlgvideosource.htm
tech.root: Multimedia
ms.assetid: 9913a9e0-13ee-4f4b-9e8b-0f2549e4ded3
ms.date: 07/01/2025
ms.keywords: _win32_capDlgVideoSource, capDlgVideoSource, capDlgVideoSource macro [Windows Multimedia], multimedia.capdlgvideosource, vfw/capDlgVideoSource
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
 - capDlgVideoSource
 - vfw/capDlgVideoSource
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
 - capDlgVideoSource
---

# capDlgVideoSource macro

## -syntax

```cpp
BOOL capDlgVideoSource(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capDlgVideoSource</b> macro displays a dialog box in which the user can control the video source. The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-dlg-videosource">WM_CAP_DLG_VIDEOSOURCE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

The Video Source dialog box is unique for each capture driver. Some capture drivers might not support a Video Source dialog box. Applications can determine if the capture driver supports this message by checking the <b>fHasDlgVideoSource</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-capdrivercaps">CAPDRIVERCAPS</a> structure.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
