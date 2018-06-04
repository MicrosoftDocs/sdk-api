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

# IWMPSubscriptionService2::serviceEvent


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>serviceEvent</b> method is called when the online store is activated or deactivated.




## -parameters




### -param event [in]

A <a href="https://msdn.microsoft.com/9d04e534-083b-4227-82aa-4f7e50a492df">WMPSubscriptionServiceEvent</a> enumeration value indicating whether the service is activated or deactivated.


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



Your code should not perform lengthy operations synchronously when Windows Media Player calls this method. Instead, you must perform time-consuming tasks on a separate worker thread.




## -see-also




<a href="https://msdn.microsoft.com/5338a3c1-c44a-4c03-a21a-6cd5cfeef064">IWMPSubscriptionService2 Interface</a>



<a href="https://msdn.microsoft.com/9d04e534-083b-4227-82aa-4f7e50a492df">WMPSubscriptionServiceEvent</a>
 

 

