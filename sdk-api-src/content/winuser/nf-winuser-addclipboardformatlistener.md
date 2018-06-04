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

# AddClipboardFormatListener function


## -description


Places the given window in the system-maintained clipboard format listener list.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window to be placed in the clipboard format listener list.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise. Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for additional details.




## -remarks



When a window has been added to the clipboard format listener list, it is posted a <a href="https://msdn.microsoft.com/1508aa22-9cf0-40a2-8cb0-ce7c8671df2c">WM_CLIPBOARDUPDATE</a> message whenever the contents of the clipboard have changed.




## -see-also




<a href="https://msdn.microsoft.com/5790fb14-473a-49fc-943b-9cc5f1170181">GetClipboardSequenceNumber</a>



<a href="https://msdn.microsoft.com/64b18bad-ebac-4e51-9806-aa288abfc112">RemoveClipboardFormatListener</a>



<a href="https://msdn.microsoft.com/1508aa22-9cf0-40a2-8cb0-ce7c8671df2c">WM_CLIPBOARDUPDATE</a>
 

 

