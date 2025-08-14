---
UID: NF:vfw.capCaptureGetSetup
title: capCaptureGetSetup macro (vfw.h)
description: The capCaptureGetSetup macro retrieves the current settings of the streaming capture parameters. You can use this macro or explicitly send the WM_CAP_GET_SEQUENCE_SETUP message.
helpviewer_keywords: ["_win32_capCaptureGetSetup","capCaptureGetSetup","capCaptureGetSetup macro [Windows Multimedia]","multimedia.capcapturegetsetup","vfw/capCaptureGetSetup"]
old-location: multimedia\capcapturegetsetup.htm
tech.root: Multimedia
ms.assetid: 198b1aae-b719-4fb8-a11d-859eaf7a4606
ms.date: 07/01/2025
ms.keywords: _win32_capCaptureGetSetup, capCaptureGetSetup, capCaptureGetSetup macro [Windows Multimedia], multimedia.capcapturegetsetup, vfw/capCaptureGetSetup
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
 - capCaptureGetSetup
 - vfw/capCaptureGetSetup
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
 - capCaptureGetSetup
---

# capCaptureGetSetup macro

## -syntax

```cpp
BOOL capCaptureGetSetup(
     hwnd,
     s,
     wSize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capCaptureGetSetup</b> macro retrieves the current settings of the streaming capture parameters. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-get-sequence-setup">WM_CAP_GET_SEQUENCE_SETUP</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param s

Pointer to a <a href="/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure.

### -param wSize

Size, in bytes, of the structure referenced by s.

## -remarks

For information about the parameters used to control streaming capture, see the <a href="/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
