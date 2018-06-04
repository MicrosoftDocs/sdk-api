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

# DdReenableDirectDrawObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/26451881-cebf-4db1-aeed-365f0dae6704">NtGdiDdReenableDirectDrawObject</a> function. It re-enables a Microsoft DirectDraw driver instance after a mode switch-style event such as a true mode switch, appearance of a full-screen Microsoft MS-DOS box, or change of display driver.



<b>GdiEntry10</b> is defined as an alias for this function.


## -parameters




### -param pDirectDrawGlobal

DirectDraw object that needs to be re-enabled.


### -param pbNewMode

Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.


## -returns



If successful (the device can be re-enabled), this function returns <b>TRUE</b>. Otherwise (for example, the display driver was changed), it returns <b>FALSE</b>.




## -remarks



Once the object has been re-enabled, the capabilities for the device can be re-queried using a call to <a href="https://msdn.microsoft.com/12acec03-cc31-4a6a-8f22-dd6f5e7fc8ef">DdQueryDirectDrawObject</a> or GdiEntry2.


Applications are advised to use the 
DirectDraw or <a href="http://msdn.microsoft.com/en-us/library/bb205147(VS.85).aspx">Direct3D</a>APIs, which automate and abstract this process in a manner independent of the operating system.





## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

