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

# IMediaEvent::RestoreDefaultHandling


## -description



The <code>RestoreDefaultHandling</code> method restores the Filter Graph Manager's default handling for a specified event.




## -parameters




### -param lEvCode [in]

Event code for which to restore default handling.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
No default handling for this event.

</td>
</tr>
</table>
 




## -remarks



By default, the Filter Graph Manager handles some events (such as <a href="https://msdn.microsoft.com/2e756dea-366c-4024-8fc8-6feabaef1954">EC_REPAINT</a>) without passing them to the application. If you call the <a href="https://msdn.microsoft.com/955d0494-8418-42a1-ab6e-2c779165f578">IMediaEvent::CancelDefaultHandling</a> method to override the default handling for an event, you can restore the default behavior by calling <code>RestoreDefaultHandling</code> with the same event code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/651561d1-4e7e-48de-9cba-769ddb553e63">IMediaEvent Interface</a>
 

 

