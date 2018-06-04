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

# ImmDisableLegacyIME function


## -description


Indicates that this thread is a Windows Store app UI thread.


## -parameters






## -returns



Returns <b>TRUE</b> if successful;   otherwise, <b>FALSE</b>. 




## -remarks



Windows Store app brokers such as explorer.exe should call this function in Windows Store app UI threads to ensure that only IMEs that are compatible with  Windows Store apps are made available.  Those Windows Store app threads that don't require IME input should call <a href="https://msdn.microsoft.com/c563fc24-3c56-40ac-8539-8336d5231537">ImmDisableIME</a> to disable IMM entirely for that thread.

The app must call this function before the first top-level window in the thread receives the <a href="_win32_wm_create_cpp">WM_CREATE</a> message. Thus, the app must call this function in one of the following places:

<ul>
<li>Any time before  <a href="_win32_createwindow_cpp">CreateWindow</a> is called to create the first top-level window.</li>
<li>In the <a href="_win32_wm_nccreate_cpp">WM_NCCREATE</a> handler for the first top-level window.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

