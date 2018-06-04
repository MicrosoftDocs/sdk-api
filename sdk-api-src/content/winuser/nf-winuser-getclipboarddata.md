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

# GetClipboardData function


## -description


Retrieves data from the clipboard in a specified format. The clipboard must have been opened previously. 


## -parameters




### -param uFormat [in]

Type: <b>UINT</b>

A clipboard format. For a description of the standard clipboard formats, see <a href="clipboard_formats.htm">Standard Clipboard Formats</a>.


## -returns



Type: <b>HANDLE</b>

If the function succeeds, the return value is the handle to a clipboard object in the specified format.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<div class="alert"><b>Caution</b>  Clipboard data is not trusted. Parse the data carefully before using it in your application.</div>
<div> </div>
An application can enumerate the available formats in advance by using the <a href="https://msdn.microsoft.com/eca6e3ca-46d1-4f1d-a13c-63542e8eb8bf">EnumClipboardFormats</a> function. 

The clipboard controls the handle that the <b>GetClipboardData</b> function returns, not the application. The application should copy the data immediately. The application must not free the handle nor leave it locked. The application must not use the handle after the <a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a> or <a href="https://msdn.microsoft.com/34658e02-cbac-4e5a-afb3-a1450274b5b1">CloseClipboard</a> function is called, or after the <a href="https://msdn.microsoft.com/45ca0c04-cf1a-4206-a05f-9957e50be89c">SetClipboardData</a> function is called with the same clipboard format. 

The system performs implicit data format conversions between certain clipboard formats when an application calls the <b>GetClipboardData</b> function. For example, if the <a href="standard_clipboard_formats.htm">CF_OEMTEXT</a> format is on the clipboard, a window can retrieve data in the <a href="standard_clipboard_formats.htm">CF_TEXT</a> format. The format on the clipboard is converted to the requested format on demand. For more information, see <a href="clipboard_formats.htm">Synthesized Clipboard Formats</a>. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Copying Information to the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<a href="https://msdn.microsoft.com/34658e02-cbac-4e5a-afb3-a1450274b5b1">CloseClipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a>



<a href="https://msdn.microsoft.com/eca6e3ca-46d1-4f1d-a13c-63542e8eb8bf">EnumClipboardFormats</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/45ca0c04-cf1a-4206-a05f-9957e50be89c">SetClipboardData</a>
 

 

