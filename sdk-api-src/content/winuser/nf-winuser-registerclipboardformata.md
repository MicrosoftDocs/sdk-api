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

# RegisterClipboardFormatA function


## -description


Registers a new clipboard format. This format can then be used as a valid clipboard format. 


## -parameters




### -param lpszFormat [in]

Type: <b>LPCTSTR</b>

The name of the new format. 


## -returns



Type: <b>UINT</b>

If the function succeeds, the return value identifies the registered clipboard format.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If a registered format with the specified name already exists, a new format is not registered and the return value identifies the existing format. This enables more than one application to copy and paste data using the same registered clipboard format. Note that the format name comparison is case-insensitive.

Registered clipboard formats are identified by values in the range 0xC000 through 0xFFFF. 

When registered clipboard formats are placed on or retrieved from the clipboard, they must be in the form of an 
				<b>HGLOBAL</b> value. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Registering a Clipboard Format</a>. 



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3f9390f0-0fcb-4654-add0-eeea8f79b3f5">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/eca6e3ca-46d1-4f1d-a13c-63542e8eb8bf">EnumClipboardFormats</a>



<a href="https://msdn.microsoft.com/58cb43df-32a5-44ed-b017-441fe18ce54b">GetClipboardFormatName</a>



<b>Reference</b>
 

 

