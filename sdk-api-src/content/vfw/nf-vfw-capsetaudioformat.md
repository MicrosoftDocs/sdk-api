---
UID: NF:vfw.capSetAudioFormat
title: capSetAudioFormat macro (vfw.h)
description: The capSetAudioFormat macro sets the audio format to use when performing streaming or step capture. You can use this macro or explicitly call the WM_CAP_SET_AUDIOFORMAT message.
helpviewer_keywords: ["_win32_capSetAudioFormat","capSetAudioFormat","capSetAudioFormat macro [Windows Multimedia]","multimedia.capsetaudioformat","vfw/capSetAudioFormat"]
old-location: multimedia\capsetaudioformat.htm
tech.root: Multimedia
ms.assetid: 9f14b76c-3b12-4dfb-937d-e8a173e077bd
ms.date: 07/01/2025
ms.keywords: _win32_capSetAudioFormat, capSetAudioFormat, capSetAudioFormat macro [Windows Multimedia], multimedia.capsetaudioformat, vfw/capSetAudioFormat
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
 - capSetAudioFormat
 - vfw/capSetAudioFormat
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
 - capSetAudioFormat
---

# capSetAudioFormat macro

## -syntax

```cpp
BOOL capSetAudioFormat(
     hwnd,
     s,
     wSize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capSetAudioFormat</b> macro sets the audio format to use when performing streaming or step capture. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-audioformat">WM_CAP_SET_AUDIOFORMAT</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param s

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> or <a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a> structure that defines the audio format.

### -param wSize

Size, in bytes, of the structure referenced by <i>psAudioFormat</i>.

## -see-also

<a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a>



<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>



<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>



<a href="/windows/desktop/Multimedia/wm-cap-set-audioformat">WM_CAP_SET_AUDIOFORMAT</a>
