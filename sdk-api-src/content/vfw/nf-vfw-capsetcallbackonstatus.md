---
UID: NF:vfw.capSetCallbackOnStatus
title: capSetCallbackOnStatus macro (vfw.h)
description: The capSetCallbackOnStatus macro sets a status callback function in the application. AVICap calls this procedure whenever the capture window status changes. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_STATUS message.
helpviewer_keywords: ["_win32_capSetCallbackOnStatus","capSetCallbackOnStatus","capSetCallbackOnStatus macro [Windows Multimedia]","multimedia.capsetcallbackonstatus","vfw/capSetCallbackOnStatus"]
old-location: multimedia\capsetcallbackonstatus.htm
tech.root: Multimedia
ms.assetid: 7024aa3e-d227-4c22-8259-6299e9205f53
ms.date: 07/01/2025
ms.keywords: _win32_capSetCallbackOnStatus, capSetCallbackOnStatus, capSetCallbackOnStatus macro [Windows Multimedia], multimedia.capsetcallbackonstatus, vfw/capSetCallbackOnStatus
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
 - capSetCallbackOnStatus
 - vfw/capSetCallbackOnStatus
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
 - capSetCallbackOnStatus
---

# capSetCallbackOnStatus macro

## -syntax

```cpp
BOOL capSetCallbackOnStatus(
     hwnd,
     fpProc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.


## -description

The <b>capSetCallbackOnStatus</b> macro sets a status callback function in the application. AVICap calls this procedure whenever the capture window status changes. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-status">WM_CAP_SET_CALLBACK_STATUS</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param fpProc

Pointer to the status callback function, of type <a href="/windows/desktop/api/vfw/nc-vfw-capstatuscallbacka">capStatusCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed status callback function.

## -remarks

Applications can optionally set a status callback function. If set, AVICap calls this procedure in the following situations:

<ul>
<li>A capture session is completed.</li>
<li>A capture driver successfully connected to a capture window.</li>
<li>An optimal palette is created.</li>
<li>The number of captured frames is reported.</li>
</ul>

## -see-also

<a href="/windows/desktop/Multimedia/creating-a-status-callback-function">Creating a Status Callback Function</a>



<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
