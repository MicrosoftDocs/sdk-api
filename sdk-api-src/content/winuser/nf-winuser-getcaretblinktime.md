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

# GetCaretBlinkTime function


## -description


Retrieves the time required to invert the caret's pixels.
          The user can set this value. 


## -parameters






## -returns



Type: <b>UINT</b>

If the function succeeds, the return value is the blink time, in milliseconds.
          

A return value of <b>INFINITE</b> indicates that the caret does not blink.

A return value is zero indicates that the function has failed.
             To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/34ff3420-a1d2-46cc-9378-4b3340bec8c8">Carets</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f3109f0f-f6b8-4ea6-9159-cc31489eaf88">SetCaretBlinkTime</a>
 

 

