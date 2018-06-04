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

# ShowCaret function


## -description


Makes the caret visible on the screen at the caret's current position. When the caret becomes visible, it begins flashing automatically. 


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the caret. If this parameter is <b>NULL</b>, <b>ShowCaret</b> searches the current task for the window that owns the caret. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>ShowCaret</b> shows the caret only if the specified window owns the caret, the caret has a shape, and the caret has not been hidden two or more times in a row. If one or more of these conditions is not met, <b>ShowCaret</b> does nothing and returns <b>FALSE</b>. 

Hiding is cumulative. If your application calls <a href="https://msdn.microsoft.com/2fab919f-11aa-429e-aaa6-89854caa7b1c">HideCaret</a> five times in a row, it must also call <b>ShowCaret</b> five times before the caret reappears. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. 


#### Examples

For an example, see <a href="using_carets.htm">Creating and Displaying a Caret</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/34ff3420-a1d2-46cc-9378-4b3340bec8c8">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f936c2cd-57a2-47ad-8be1-a2d99dcbe709">CreateCaret</a>



<a href="https://msdn.microsoft.com/ed434af6-1146-41b7-a4dc-8b5215a9ff43">DestroyCaret</a>



<a href="https://msdn.microsoft.com/14786dc7-bdd2-45e5-8073-b8dc3f5d30de">GetCaretPos</a>



<a href="https://msdn.microsoft.com/2fab919f-11aa-429e-aaa6-89854caa7b1c">HideCaret</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0a8d4ca6-d409-4468-b29a-552adbea0918">SetCaretPos</a>
 

 

