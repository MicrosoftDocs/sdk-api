---
UID: NF:vfw.capFileAlloc
title: capFileAlloc macro (vfw.h)
description: The capFileAlloc macro creates (preallocates) a capture file of a specified size. You can use this macro or explicitly send the WM_CAP_FILE_ALLOCATE message.
helpviewer_keywords: ["_win32_capFileAlloc","capFileAlloc","capFileAlloc macro [Windows Multimedia]","multimedia.capfilealloc","vfw/capFileAlloc"]
old-location: multimedia\capfilealloc.htm
tech.root: Multimedia
ms.assetid: 579c5406-f44a-4ea2-9822-f09a890489fb
ms.date: 07/01/2025
ms.keywords: _win32_capFileAlloc, capFileAlloc, capFileAlloc macro [Windows Multimedia], multimedia.capfilealloc, vfw/capFileAlloc
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
 - capFileAlloc
 - vfw/capFileAlloc
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
 - capFileAlloc
---

# capFileAlloc macro

## -syntax

```cpp
BOOL capFileAlloc(
     hwnd,
     dwSize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.If an error occurs and an error callback function is set using the **capSetCallbackOnError** macro, the error callback function is called.


## -description

The <b>capFileAlloc</b> macro creates (preallocates) a capture file of a specified size. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-file-allocate">WM_CAP_FILE_ALLOCATE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param dwSize

Size, in bytes, to create the capture file.

## -remarks

You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
