---
UID: NF:vfw.capGetAudioFormatSize
title: capGetAudioFormatSize macro (vfw.h)
description: The capGetAudioFormatSize macro obtains the size of the audio format. You can use this macro or explicitly call the WM_CAP_GET_AUDIOFORMAT message.
helpviewer_keywords: ["_win32_capGetAudioFormatSize","capGetAudioFormatSize","capGetAudioFormatSize macro [Windows Multimedia]","multimedia.capgetaudioformatsize","vfw/capGetAudioFormatSize"]
old-location: multimedia\capgetaudioformatsize.htm
tech.root: Multimedia
ms.assetid: 6f2dbedb-bece-4082-aa68-c2390c75b4d7
ms.date: 07/01/2025
ms.keywords: _win32_capGetAudioFormatSize, capGetAudioFormatSize, capGetAudioFormatSize macro [Windows Multimedia], multimedia.capgetaudioformatsize, vfw/capGetAudioFormatSize
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
 - capGetAudioFormatSize
 - vfw/capGetAudioFormatSize
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
 - capGetAudioFormatSize
---

# capGetAudioFormatSize macro

## -syntax

```cpp
DWORD capGetAudioFormatSize(
     hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the size, in bytes, of the audio format.


## -description

The <b>capGetAudioFormatSize</b> macro obtains the size of the audio format. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-get-audioformat">WM_CAP_GET_AUDIOFORMAT</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
