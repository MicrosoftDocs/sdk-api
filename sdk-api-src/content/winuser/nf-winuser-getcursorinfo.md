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

# GetCursorInfo function


## -description


Retrieves information about the global cursor.


## -parameters




### -param pci [in, out]

Type: <b>PCURSORINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/acd66f67-c95d-49fa-8f61-fdae3c86b432">CURSORINFO</a> structure that receives the information. Note that you must set the <b>cbSize</b> member to <code>sizeof(CURSORINFO)</code> before calling this function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/acd66f67-c95d-49fa-8f61-fdae3c86b432">CURSORINFO</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/863e0735-a2d4-4962-99d8-bb6037770c50">GetGUIThreadInfo</a>



<b>Reference</b>
 

 

