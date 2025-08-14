---
UID: NF:winuser.GetGestureInfo
title: GetGestureInfo function (winuser.h)
description: Retrieves a GESTUREINFO structure given a handle to the gesture information.
helpviewer_keywords: ["GetGestureInfo","GetGestureInfo function [Windows Touch]","wintouch.getgestureinfo","winuser/GetGestureInfo"]
old-location: wintouch\getgestureinfo.htm
tech.root: wintouch
ms.assetid: 407ed585-09aa-4174-8907-8bb9590f1795
ms.date: 12/05/2018
ms.keywords: GetGestureInfo, GetGestureInfo function [Windows Touch], wintouch.getgestureinfo, winuser/GetGestureInfo
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - GetGestureInfo
 - winuser/GetGestureInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetGestureInfo
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# GetGestureInfo function


## -description

Retrieves a <a href="/windows/desktop/api/winuser/ns-winuser-gestureinfo">GESTUREINFO</a>  structure given a handle to 
  the gesture information.

## -parameters

### -param hGestureInfo [in]

The gesture information handle.

### -param pGestureInfo [out]

A pointer to the gesture information structure.

## -returns

If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The <b>cbSize</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-gestureinfo">GESTUREINFO</a> structure passed in to the function must be set
    before the function is called.  Otherwise, calls to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <b>ERROR_INVALID_PARAMETER</b> (87 in decimal).
   If an application processes a <a href="/windows/desktop/wintouch/wm-gesture">WM_GESTURE</a> message, it is responsible for
   closing the handle using <a href="/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle">CloseGestureInfoHandle</a>. Failure to do so may result in
   process memory leaks.
  

If the message is passed to <a href="/windows/win32/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>, or is forwarded using
   one of the PostMessage or SendMessage classes of API functions, the handle
   is transferred with the message and need not be closed by the application.
  


#### Examples


```cpp

    GESTUREINFO gestureInfo = {0};
    gestureInfo.cbSize = sizeof(gestureInfo);
    BOOL bResult = GetGestureInfo((HGESTUREINFO)lParam, &gestureInfo);

    if (!bResult){                
        DWORD err = GetLastError();                                       
    }
    
```

## -see-also

<a href="/windows/desktop/wintouch/mtgfunctions">Functions</a>



<a href="/windows/desktop/wintouch/guide-multi-touch-gestures">Programming Guide for Gestures</a>
