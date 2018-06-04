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

# IMFMediaSession::Close


## -description



Closes the Media Session and releases all of the resources it is using.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The Media Session has been shut down.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. When the operation completes, the Media Session sends an <a href="https://msdn.microsoft.com/d1056ce7-5527-428a-8ace-e1c10a2124a5">MESessionClosed</a> event.

After the <b>Close</b> method is called, the only valid methods on the Media Session are the following:

<ul>
<li>

<a href="https://msdn.microsoft.com/16444da2-68f2-4d94-8c6f-9e512d51e5e9">IMFMediaSession::GetClock</a>


</li>
<li>

<a href="https://msdn.microsoft.com/6899dbe2-a684-487f-ab56-8631b3d5a033">IMFMediaSession::GetFullTopology</a>


</li>
<li>

<a href="https://msdn.microsoft.com/3534cfb9-23ff-42a6-a3db-b5032d427cf2">IMFMediaSession::GetSessionCapabilities</a>


</li>
<li>

<a href="https://msdn.microsoft.com/5b9663c2-e32e-4075-b397-59ae01558e15">IMFMediaSession::Shutdown</a>


</li>
</ul>
All other methods return MF_E_INVALIDREQUEST, or else queue an event with that error code.




## -see-also




<a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a>
 

 

