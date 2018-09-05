---
UID: NF:winuser.GetGestureInfo
title: GetGestureInfo function
author: windows-sdk-content
description: Retrieves a GESTUREINFO structure given a handle to the gesture information.
old-location: wintouch\getgestureinfo.htm
old-project: wintouch
ms.assetid: 407ed585-09aa-4174-8907-8bb9590f1795
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetGestureInfo, GetGestureInfo function [Windows Touch], wintouch.getgestureinfo, winuser/GetGestureInfo
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
 - GetGestureInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetGestureInfo function


## -description


Retrieves a <a href="https://msdn.microsoft.com/f5b8b530-ff1e-4d78-a12f-86990fe9ac88">GESTUREINFO</a>  structure given a handle to 
  the gesture information.
  


## -parameters




### -param hGestureInfo [in]

The gesture information handle.


### -param pGestureInfo [out]

A pointer to the gesture information structure.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks



The <b>cbSize</b> member of the <a href="https://msdn.microsoft.com/f5b8b530-ff1e-4d78-a12f-86990fe9ac88">GESTUREINFO</a> structure passed in to the function must be set
    before the function is called.  Otherwise, calls to <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> will return <b>ERROR_INVALID_PARAMETER</b> (87 in decimal).
   If an application processes a <a href="https://msdn.microsoft.com/4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8">WM_GESTURE</a> message, it is responsible for
   closing the handle using <a href="https://msdn.microsoft.com/f2bf98b2-a4f7-4b63-b9ae-b2534415cb4b">CloseGestureInfoHandle</a>. Failure to do so may result in
   process memory leaks.
  

If the message is passed to <a href="http://go.microsoft.com/fwlink/p/?linkid=136637">DefWindowProc</a>, or is forwarded using
   one of the PostMessage or SendMessage classes of API functions, the handle
   is transferred with the message and need not be closed by the application.
  


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    GESTUREINFO gestureInfo = {0};
    gestureInfo.cbSize = sizeof(gestureInfo);
    BOOL bResult = GetGestureInfo((HGESTUREINFO)lParam, &amp;gestureInfo);

    if (!bResult){                
        DWORD err = GetLastError();                                       
    }
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/830031d1-eb8d-45d4-b66e-3f4fbb96ae13">Functions</a>



<a href="https://msdn.microsoft.com/afd61b18-4e54-44c5-9b71-74908c76c7ac">Programming Guide for Gestures</a>
 

 

