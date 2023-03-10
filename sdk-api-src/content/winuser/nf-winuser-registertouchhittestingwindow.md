---
UID: NF:winuser.RegisterTouchHitTestingWindow
title: RegisterTouchHitTestingWindow function (winuser.h)
description: Registers a window to process the WM_TOUCHHITTESTING notification.
helpviewer_keywords: ["RegisterTouchHitTestingWindow","RegisterTouchHitTestingWindow function","input_touchhittest.registertouchhittestingwindow","touch_hittest.registertouchhittestingwindow","winuser/RegisterTouchHitTestingWindow"]
old-location: input_touchhittest\registertouchhittestingwindow.htm
tech.root: controls
ms.assetid: 52e48cea-b5c7-405f-8df6-26052304b62c
ms.date: 12/05/2018
ms.keywords: RegisterTouchHitTestingWindow, RegisterTouchHitTestingWindow function, input_touchhittest.registertouchhittestingwindow, touch_hittest.registertouchhittestingwindow, winuser/RegisterTouchHitTestingWindow
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterTouchHitTestingWindow
 - winuser/RegisterTouchHitTestingWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Touch-HitTest-l1-1-0.dll
 - MinUser.dll
api_name:
 - RegisterTouchHitTestingWindow
---

# RegisterTouchHitTestingWindow function


## -description

Registers a window to process the  

<a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a> notification.

## -parameters

### -param hwnd [in]

The window that receives the <a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a>  notification.

### -param value [in]

One of the following values: 

<ul>
<li>
<a href="/previous-versions/windows/desktop/input_touchhittest/hit-testing-behaviors">TOUCH_HIT_TESTING_CLIENT</a>: Send <a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a>  messages to the target window.</li>
<li>
<a href="/previous-versions/windows/desktop/input_touchhittest/hit-testing-behaviors">TOUCH_HIT_TESTING_DEFAULT</a>: Don't send <a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a>  messages to the target window but continue to send the messages to child windows.
</li>
<li>
<a href="/previous-versions/windows/desktop/input_touchhittest/hit-testing-behaviors">TOUCH_HIT_TESTING_NONE</a>: Don't send <a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a>  messages to the target window or child windows.
</li>
</ul>

## -returns

If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/input_touchhittest/functions">Functions</a>