---
UID: NF:winuser.CloseGestureInfoHandle
title: CloseGestureInfoHandle function (winuser.h)
description: Closes resources associated with a gesture information handle.
helpviewer_keywords: ["CloseGestureInfoHandle","CloseGestureInfoHandle function [Windows Touch]","wintouch.closegestureinfohandle","winuser/CloseGestureInfoHandle"]
old-location: wintouch\closegestureinfohandle.htm
tech.root: wintouch
ms.assetid: f2bf98b2-a4f7-4b63-b9ae-b2534415cb4b
ms.date: 12/05/2018
ms.keywords: CloseGestureInfoHandle, CloseGestureInfoHandle function [Windows Touch], wintouch.closegestureinfohandle, winuser/CloseGestureInfoHandle
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
 - CloseGestureInfoHandle
 - winuser/CloseGestureInfoHandle
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
 - CloseGestureInfoHandle
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# CloseGestureInfoHandle function


## -description

Closes resources associated with a gesture information handle.

## -parameters

### -param hGestureInfo

The gesture information handle.

## -returns

If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

If an application processes a <a href="/windows/desktop/wintouch/wm-gesture">WM_GESTURE</a> message, it is responsible for
   closing the handle using this function. Failure to do so may result in
   process memory leaks.
  

If the message is passed to <a href="/windows/win32/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>, or is forwarded using
   one of the PostMessage or SendMessage classes of API functions, the handle
   is transferred with the message and need not be closed by the application.
  


#### Examples

The following code shows a handler that closes the <a href="/windows/desktop/api/winuser/ns-winuser-gestureinfo">GESTUREINFO</a> handle if the gesture has been handled.


```cpp
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }

```

## -see-also

<a href="/windows/desktop/wintouch/mtgfunctions">Functions</a>



<a href="/windows/desktop/wintouch/guide-multi-touch-gestures">Programming Guide for Gestures</a>
