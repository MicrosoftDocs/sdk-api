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

# DdResetVisrgn function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/286f1c06-c27b-42bd-aecc-3a6923e3df29">NtGdiDdResetVisrgn</a> function and enables timely user-mode information on the clipping region for windows on the desktop.

<b>GdiEntry6</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceLocal

Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset. See the DDK documentation for details.


### -param hWnd

Reserved.


## -returns



If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks



Clipping can change asynchronously from the point of view of user-mode threads. 
The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes. A call to this function records this counter with every existing DirectDraw primary surface on the system.

At any later time when one of these primary surfaces is modified by a <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a> or <a href="http://msdn.microsoft.com/en-us/library/ms858221.aspx">IDirectDrawSurface7::Lock</a> operation (see DDK documentation), the counter recorded with the surface is compared with the global counter. If these values are different, an error code DDERR_VISRGNCHANGED is returned to the user-mode code. The user-mode code will then re-query the current clipping for the desktop, call <a href="https://msdn.microsoft.com/286f1c06-c27b-42bd-aecc-3a6923e3df29">NtGdiDdResetVisrgn</a>, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping. Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.

Applications are advised to use the <a href="http://msdn.microsoft.com/en-us/library/aa919448.aspx">IDirectDrawClipper</a> interface or <a href="http://msdn.microsoft.com/en-us/library/ms889707.aspx">IDirect3DDevice8::Present</a> method to handle asynchronous clipping changes. These constructs implement asynchronous clipping in an automated and operating-system-independent way.





## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

