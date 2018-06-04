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

# IMFSourceOpenMonitor::OnSourceEvent


## -description



Called by the network source when the open operation begins or ends.




## -parameters




### -param pEvent [in]

Pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface.


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
</table>
 




## -remarks



The networks source calls this method with the following event types.

<ul>
<li>

<a href="https://msdn.microsoft.com/0844ac10-cc5b-4e7f-92df-3a5901c72148">MEConnectStart</a>


</li>
<li>

<a href="https://msdn.microsoft.com/737aec32-24f4-4825-ad34-8d2fc889bc09">MEConnectEnd</a>


</li>
</ul>
For more information, see <a href="https://msdn.microsoft.com/46869f52-323c-41ec-95f7-e7e5d177b782">How to Get Events from the Network Source</a>.




## -see-also




<a href="https://msdn.microsoft.com/9145910b-81f1-4fd1-8f6f-d6273e0edde6">IMFSourceOpenMonitor</a>
 

 

