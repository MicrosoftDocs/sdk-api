---
UID: NF:vfw.capFileSaveDIB
title: capFileSaveDIB macro (vfw.h)
description: The capFileSaveDIB macro copies the current frame to a DIB file. You can use this macro or explicitly call the WM_CAP_FILE_SAVEDIB message.
helpviewer_keywords: ["_win32_capFileSaveDIB","capFileSaveDIB","capFileSaveDIB macro [Windows Multimedia]","multimedia.capfilesavedib","vfw/capFileSaveDIB"]
old-location: multimedia\capfilesavedib.htm
tech.root: Multimedia
ms.assetid: bab1c97d-e84e-43ff-9b66-79b903a610eb
ms.date: 07/01/2025
ms.keywords: _win32_capFileSaveDIB, capFileSaveDIB, capFileSaveDIB macro [Windows Multimedia], multimedia.capfilesavedib, vfw/capFileSaveDIB
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
 - capFileSaveDIB
 - vfw/capFileSaveDIB
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
 - capFileSaveDIB
---

# capFileSaveDIB macro

## -syntax

```cpp
BOOL capFileSaveDIB(
     hwnd,
     szName
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.If an error occurs and an error callback function is set using the **capSetCallbackOnError** macro, the error callback function is called.


## -description

The <b>capFileSaveDIB</b> macro copies the current frame to a DIB file. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-file-savedib">WM_CAP_FILE_SAVEDIB</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param szName

Pointer to the null-terminated string that contains the name of the destination DIB file.

## -remarks

If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
