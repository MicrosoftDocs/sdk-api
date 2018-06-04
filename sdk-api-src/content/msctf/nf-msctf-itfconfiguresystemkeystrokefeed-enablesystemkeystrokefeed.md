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

# ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed


## -description




## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There was no corresponding call to DisableSystemKeystrokeFeed.

</td>
</tr>
</table>
 




## -remarks



By default, the TSF manager will process keystrokes and pass them to the text services. An application prevents this by calling <b>DisableSystemKeystrokeFeed</b> .

Calls to <b>DisableSystemKeystrokeFeed</b> are cumulative, so every call to <b>DisableSystemKeystrokeFeed</b> requires a subsequent call to <b>EnableSystemKeystrokeFeed</b>. Calling <b>EnableSystemKeystrokeFeed</b> will not enable keystroke processing if <b>DisableSystemKeystrokeFeed</b> is called more than once.




## -see-also




<a href="https://msdn.microsoft.com/9b15d628-87aa-4e20-b9c3-fb29a79683cb">ITfConfigureSystemKeystrokeFeed</a>



<a href="https://msdn.microsoft.com/6bdca5cc-84b4-4184-a8cc-76dddc573b35">ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed
      </a>
 

 

