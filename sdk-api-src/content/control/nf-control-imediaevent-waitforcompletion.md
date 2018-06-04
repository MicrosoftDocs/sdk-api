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

# IMediaEvent::WaitForCompletion


## -description



The <code>WaitForCompletion</code> method waits for the filter graph to render all available data. The filter graph must be running or the method fails.




## -parameters




### -param msTimeout [in]

Time-out interval, in milliseconds. Pass zero to return immediately. Pass the value INFINITE to block indefinitely.


### -param pEvCode [out]

Pointer to a variable that receives an event code. See Remarks for more information.


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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Time-out expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not running.

</td>
</tr>
</table>
 




## -remarks



This method blocks until the time-out expires, or one of the following events occurs:

<ul>
<li>
<a href="https://msdn.microsoft.com/46037d53-085d-4fd0-91a0-408702cbfce5">EC_COMPLETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b41546ce-cfac-4cc3-a9ad-413ae2d5d6d5">EC_ERRORABORT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/974a9c3e-cfc9-4608-9f98-732aeaa0a752">EC_USERABORT</a>
</li>
</ul>
During the wait, the method discards all other event notifications.

If the return value is S_OK, the <i>pEvCode</i> parameter receives the event code that ended the wait. When the method returns, the filter graph is still running. The application can pause or stop the graph, as appropriate.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/651561d1-4e7e-48de-9cba-769ddb553e63">IMediaEvent Interface</a>
 

 

