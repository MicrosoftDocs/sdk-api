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

# GetClipboardViewer function


## -description


Retrieves the handle to the first window in the clipboard viewer chain.


## -parameters






## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the first window in the clipboard viewer chain. 

If there is no clipboard viewer, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/96c06602-05ec-4f38-a53b-1729f2c1ce4f">GetClipboardOwner</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b1c9c0eb-388f-4fa1-9744-8ebd324cec4f">SetClipboardViewer</a>
 

 

