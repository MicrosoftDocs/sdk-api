---
UID: NF:vfw.capFileSaveAs
title: capFileSaveAs macro (vfw.h)
description: The capFileSaveAs macro copies the contents of the capture file to another file. You can use this macro or explicitly call the WM_CAP_FILE_SAVEAS message.
helpviewer_keywords: ["_win32_capFileSaveAs","capFileSaveAs","capFileSaveAs macro [Windows Multimedia]","multimedia.capfilesaveas","vfw/capFileSaveAs"]
old-location: multimedia\capfilesaveas.htm
tech.root: Multimedia
ms.assetid: 164bb345-c092-4adb-8f0f-83e31d36390f
ms.date: 07/01/2025
ms.keywords: _win32_capFileSaveAs, capFileSaveAs, capFileSaveAs macro [Windows Multimedia], multimedia.capfilesaveas, vfw/capFileSaveAs
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
 - capFileSaveAs
 - vfw/capFileSaveAs
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
 - capFileSaveAs
---

# capFileSaveAs macro

## -syntax

```cpp
BOOL capFileSaveAs(
     hwnd,
     szName
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.If an error occurs and an error callback function is set using the **capSetCallbackOnError** macro, the error callback function is called.


## -description

The <b>capFileSaveAs</b> macro copies the contents of the capture file to another file. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-file-saveas">WM_CAP_FILE_SAVEAS</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param szName

Pointer to the null-terminated string that contains the name of the destination file used to copy the file.

## -remarks

This message does not change the name or contents of the current capture file.

If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.

Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data. This message copies only the portion of the file containing the capture data.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
