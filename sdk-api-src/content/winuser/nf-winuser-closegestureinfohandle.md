---
UID: NF:winuser.CloseGestureInfoHandle
title: CloseGestureInfoHandle function
author: windows-sdk-content
description: Closes resources associated with a gesture information handle.
old-location: wintouch\closegestureinfohandle.htm
old-project: wintouch
ms.assetid: f2bf98b2-a4f7-4b63-b9ae-b2534415cb4b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CloseGestureInfoHandle, CloseGestureInfoHandle function [Windows Touch], wintouch.closegestureinfohandle, winuser/CloseGestureInfoHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - CloseGestureInfoHandle
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CloseGestureInfoHandle function


## -description


Closes resources associated with a gesture information handle.


## -parameters




### -param hGestureInfo

The gesture information handle.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks



If an application processes a <a href="https://msdn.microsoft.com/4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8">WM_GESTURE</a> message, it is responsible for
   closing the handle using this function. Failure to do so may result in
   process memory leaks.
  

If the message is passed to <a href="http://go.microsoft.com/fwlink/p/?linkid=136637">DefWindowProc</a>, or is forwarded using
   one of the PostMessage or SendMessage classes of API functions, the handle
   is transferred with the message and need not be closed by the application.
  


#### Examples

The following code shows a handler that closes the <a href="https://msdn.microsoft.com/f5b8b530-ff1e-4d78-a12f-86990fe9ac88">GESTUREINFO</a> handle if the gesture has been handled.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&amp;gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &amp;gi);
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
        if (dwErr &gt; 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/830031d1-eb8d-45d4-b66e-3f4fbb96ae13">Functions</a>



<a href="https://msdn.microsoft.com/afd61b18-4e54-44c5-9b71-74908c76c7ac">Programming Guide for Gestures</a>
 

 

