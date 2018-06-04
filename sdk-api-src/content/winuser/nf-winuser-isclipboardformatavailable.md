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

# IsClipboardFormatAvailable function


## -description


Determines whether the clipboard contains data in the specified format. 


## -parameters




### -param format [in]

Type: <b>UINT</b>

A standard or registered clipboard format. For a description of the standard clipboard formats, see <a href="https://msdn.microsoft.com/f0af4e61-7ef1-4263-b2c5-e4114515124f">Standard Clipboard Formats</a> . 


## -returns



Type: <b>BOOL</b>

If the clipboard format is available, the return value is nonzero.

If the clipboard format is not available, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Typically, an application that recognizes only one clipboard format would call this function when processing the <a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a> or <a href="https://msdn.microsoft.com/08ae1a78-5e68-488c-9b77-ee42044ca3ab">WM_INITMENUPOPUP</a> message. The application would then enable or disable the Paste menu item, depending on the return value. Applications that recognize more than one clipboard format should use the <a href="https://msdn.microsoft.com/7ece4b0e-2374-4b49-b4e9-278c3317f935">GetPriorityClipboardFormat</a> function for this purpose. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Pasting Information from the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3f9390f0-0fcb-4654-add0-eeea8f79b3f5">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/eca6e3ca-46d1-4f1d-a13c-63542e8eb8bf">EnumClipboardFormats</a>



<a href="https://msdn.microsoft.com/7ece4b0e-2374-4b49-b4e9-278c3317f935">GetPriorityClipboardFormat</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/892add91-a937-4602-86d2-5e5550a81872">RegisterClipboardFormat</a>



<a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a>



<a href="https://msdn.microsoft.com/08ae1a78-5e68-488c-9b77-ee42044ca3ab">WM_INITMENUPOPUP</a>
 

 

