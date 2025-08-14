---
UID: NF:vfw.capSetCallbackOnError
title: capSetCallbackOnError macro (vfw.h)
description: The capSetCallbackOnError macro sets an error callback function in the client application. AVICap calls this procedure when errors occur. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_ERROR message.
helpviewer_keywords: ["_win32_capSetCallbackOnError","capSetCallbackOnError","capSetCallbackOnError macro [Windows Multimedia]","multimedia.capsetcallbackonerror","vfw/capSetCallbackOnError"]
old-location: multimedia\capsetcallbackonerror.htm
tech.root: Multimedia
ms.assetid: 1f9d3dba-be6d-4f7d-a80c-5bca8632e13f
ms.date: 07/01/2025
ms.keywords: _win32_capSetCallbackOnError, capSetCallbackOnError, capSetCallbackOnError macro [Windows Multimedia], multimedia.capsetcallbackonerror, vfw/capSetCallbackOnError
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
 - capSetCallbackOnError
 - vfw/capSetCallbackOnError
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
 - capSetCallbackOnError
---

# capSetCallbackOnError macro

## -syntax

```cpp
BOOL capSetCallbackOnError(
     hwnd,
     fpProc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.


## -description

The <b>capSetCallbackOnError</b> macro sets an error callback function in the client application. AVICap calls this procedure when errors occur. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-error">WM_CAP_SET_CALLBACK_ERROR</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param fpProc

Pointer to the error callback function, of type <a href="/windows/desktop/api/vfw/nc-vfw-caperrorcallbacka">capErrorCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed error callback function.

## -remarks

Applications can optionally set an error callback function. If set, AVICap calls the error procedure in the following situations:

<ul>
<li>The disk is full.</li>
<li>A capture window cannot be connected with a capture driver.</li>
<li>A waveform-audio device cannot be opened.</li>
<li>The number of frames dropped during capture exceeds the specified percentage.</li>
<li>The frames cannot be captured due to vertical synchronization interrupt problems.</li>
</ul>

## -see-also

<a href="/windows/desktop/Multimedia/creating-an-error-callback-function">Creating an Error Callback Function</a>



<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>



<a href="/windows/desktop/Multimedia/wm-cap-set-callback-error">WM_CAP_SET_CALLBACK_ERROR</a>



<a href="/windows/desktop/api/vfw/nc-vfw-caperrorcallbacka">capErrorCallback</a>
