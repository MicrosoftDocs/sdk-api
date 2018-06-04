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

# OpenClipboard function


## -description


Opens the clipboard for examination and prevents other applications from modifying the clipboard content. 


## -parameters




### -param hWndNewOwner [in, optional]

Type: <b>HWND</b>

A handle to the window to be associated with the open clipboard. If this parameter is <b>NULL</b>, the open clipboard is associated with the current task. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>OpenClipboard</b> fails if another window has the clipboard open. 

An application should call the <a href="https://msdn.microsoft.com/34658e02-cbac-4e5a-afb3-a1450274b5b1">CloseClipboard</a> function after every successful call to <b>OpenClipboard</b>. 

The window identified by the 
				<i>hWndNewOwner</i> parameter does not become the clipboard owner unless the <a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a> function is called. 

If an application calls <b>OpenClipboard</b> with hwnd set to <b>NULL</b>, <a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a> sets the clipboard owner to <b>NULL</b>; this causes <a href="https://msdn.microsoft.com/45ca0c04-cf1a-4206-a05f-9957e50be89c">SetClipboardData</a> to fail.


#### Examples

For an example, see <a href="using_the_clipboard.htm">Copying Information to the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<a href="https://msdn.microsoft.com/34658e02-cbac-4e5a-afb3-a1450274b5b1">CloseClipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a>



<b>Reference</b>
 

 

