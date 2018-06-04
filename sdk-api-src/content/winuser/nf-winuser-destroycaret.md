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

# DestroyCaret function


## -description


Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen. 


## -parameters






## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>DestroyCaret</b> destroys the caret only if a window in the current task owns the caret. If a window that is not in the current task owns the caret, <b>DestroyCaret</b> does nothing and returns <b>FALSE</b>. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. 

For an example, see <a href="using_carets.htm">Destroying a Caret</a>




## -see-also




<a href="https://msdn.microsoft.com/34ff3420-a1d2-46cc-9378-4b3340bec8c8">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f936c2cd-57a2-47ad-8be1-a2d99dcbe709">CreateCaret</a>



<a href="https://msdn.microsoft.com/2fab919f-11aa-429e-aaa6-89854caa7b1c">HideCaret</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1a3a141e-9b5a-495a-8138-b9522933499f">ShowCaret</a>
 

 

