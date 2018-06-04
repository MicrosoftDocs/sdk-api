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

# CreateIconIndirect function


## -description


Creates an icon or cursor from an <a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a> structure.


## -parameters




### -param piconinfo [in]

Type: <b>PICONINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a> structure the function uses to create the icon or cursor. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor that is created.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The system copies the bitmaps in the <a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a> structure before creating the icon or cursor. Because the system may temporarily select the bitmaps in a device context, the <b>hbmMask</b> and <b>hbmColor</b> members of the <b>ICONINFO</b> structure should not already be selected into a device context. The application must continue to manage the original bitmaps and delete them when they are no longer necessary. 

When you are finished using the icon, destroy it using the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

