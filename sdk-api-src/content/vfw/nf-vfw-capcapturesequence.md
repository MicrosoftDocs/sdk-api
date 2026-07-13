---
UID: NF:vfw.capCaptureSequence
title: capCaptureSequence macro (vfw.h)
description: The capCaptureSequence macro initiates streaming video and audio capture to a file. You can use this macro or explicitly send the WM_CAP_SEQUENCE message.
helpviewer_keywords: ["_win32_capCaptureSequence","capCaptureSequence","capCaptureSequence macro [Windows Multimedia]","multimedia.capcapturesequence","vfw/capCaptureSequence"]
old-location: multimedia\capcapturesequence.htm
tech.root: Multimedia
ms.assetid: cb4adf31-504a-46ee-b05e-768bdfde4b8f
ms.date: 07/01/2025
ms.keywords: _win32_capCaptureSequence, capCaptureSequence, capCaptureSequence macro [Windows Multimedia], multimedia.capcapturesequence, vfw/capCaptureSequence
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
 - capCaptureSequence
 - vfw/capCaptureSequence
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
 - capCaptureSequence
---

# capCaptureSequence macro

## -syntax

```cpp
BOOL capCaptureSequence(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.If an error occurs and an error callback function is set using the **capSetCallbackOnError** macro, the error callback function is called.


## -description

The <b>capCaptureSequence</b> macro initiates streaming video and audio capture to a file. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-sequence">WM_CAP_SEQUENCE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

If you want to alter the parameters controlling streaming capture, use the <a href="/windows/desktop/api/vfw/nf-vfw-capcapturesetsetup">capCaptureSetSetup</a> macro prior to starting the capture.

By default, the capture window does not allow other applications to continue running during capture. To override this, either set the <b>fYield</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure to <b>TRUE</b>, or install a yield callback function.

During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions. To install callback procedures for these notifications, use the following macros:

<ul>
<li>
<a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonerror">capSetCallbackOnError</a>
</li>
<li>
<a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonstatus">capSetCallbackOnStatus</a>
</li>
<li>
<a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonvideostream">capSetCallbackOnVideoStream</a>
</li>
<li>
<a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonwavestream">capSetCallbackOnWaveStream</a>
</li>
<li>
<a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonyield">capSetCallbackOnYield</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
