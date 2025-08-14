---
UID: NF:vfw.capEditCopy
title: capEditCopy macro (vfw.h)
description: The capEditCopy macro copies the contents of the video frame buffer and associated palette to the clipboard. You can use this macro or explicitly send the WM_CAP_EDIT_COPY message.
helpviewer_keywords: ["_win32_capEditCopy","capEditCopy","capEditCopy macro [Windows Multimedia]","multimedia.capeditcopy","vfw/capEditCopy"]
old-location: multimedia\capeditcopy.htm
tech.root: Multimedia
ms.assetid: 25b16107-b2ec-4e16-a596-10708dbc639d
ms.date: 07/01/2025
ms.keywords: _win32_capEditCopy, capEditCopy, capEditCopy macro [Windows Multimedia], multimedia.capeditcopy, vfw/capEditCopy
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
 - capEditCopy
 - vfw/capEditCopy
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
 - capEditCopy
---

# capEditCopy macro

## -syntax

```cpp
BOOL capEditCopy(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capEditCopy</b> macro copies the contents of the video frame buffer and associated palette to the clipboard. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-edit-copy">WM_CAP_EDIT_COPY</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
