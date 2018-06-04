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

# GetClipboardOwner function


## -description


Retrieves the window handle of the current owner of the clipboard. 


## -parameters






## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that owns the clipboard. 

If the clipboard is not owned, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The clipboard can still contain data even if the clipboard is not currently owned. 

In general, the clipboard owner is the window that last placed data in clipboard. The <a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a> function assigns clipboard ownership. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Example of a Clipboard Viewer</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a>



<a href="https://msdn.microsoft.com/700bee1f-1bed-4fc8-a4ce-7a48bd05e90b">GetClipboardViewer</a>



<b>Reference</b>
 

 

