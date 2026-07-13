---
UID: NF:vfw.capSetCallbackOnYield
title: capSetCallbackOnYield macro (vfw.h)
description: The capSetCallbackOnYield macro sets a callback function in the application. AVICap calls this procedure when the capture window yields during streaming capture. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_YIELD message.
helpviewer_keywords: ["_win32_capSetCallbackOnYield","capSetCallbackOnYield","capSetCallbackOnYield macro [Windows Multimedia]","multimedia.capsetcallbackonyield","vfw/capSetCallbackOnYield"]
old-location: multimedia\capsetcallbackonyield.htm
tech.root: Multimedia
ms.assetid: efddbcbc-f1e3-451c-928e-984eea187de2
ms.date: 07/01/2025
ms.keywords: _win32_capSetCallbackOnYield, capSetCallbackOnYield, capSetCallbackOnYield macro [Windows Multimedia], multimedia.capsetcallbackonyield, vfw/capSetCallbackOnYield
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
 - capSetCallbackOnYield
 - vfw/capSetCallbackOnYield
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
 - capSetCallbackOnYield
---

# capSetCallbackOnYield macro

## -syntax

```cpp
BOOL capSetCallbackOnYield(
     hwnd,
     fpProc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.


## -description

The <b>capSetCallbackOnYield</b> macro sets a callback function in the application. AVICap calls this procedure when the capture window yields during streaming capture. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-yield">WM_CAP_SET_CALLBACK_YIELD</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param fpProc

Pointer to the yield callback function, of type <a href="/windows/desktop/api/vfw/nc-vfw-capyieldcallback">capYieldCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed yield callback function.

## -remarks

Applications can optionally set a yield callback function. The yield callback function is called at least once for each video frame captured during streaming capture. If a yield callback function is installed, it will be called regardless of the state of the <b>fYield</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure.

If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session. It can be disabled after streaming capture ends.

Applications typically perform some type of message processing in the callback function consisting of a <a href="/windows/win32/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, <a href="/windows/win32/api/winuser/nf-winuser-translatemessage">TranslateMessage</a>, <a href="/windows/win32/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a> loop, as in the message loop of a <a href="/windows/win32/api/winbase/nf-winbase-winmain">WinMain</a> function. The yield callback function must also filter and remove messages that can cause reentrancy problems.

An application typically returns <b>TRUE</b> in the yield procedure to continue streaming capture. If a yield callback function returns <b>FALSE</b>, the capture window stops the capture process.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
