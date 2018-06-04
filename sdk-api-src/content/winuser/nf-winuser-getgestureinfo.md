---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/afd61b18-4e54-44c5-9b71-74908c76c7ac">Programming Guide for Gestures</a>
 

 

