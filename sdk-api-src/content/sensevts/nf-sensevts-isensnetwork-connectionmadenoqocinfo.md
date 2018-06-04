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

# ISensNetwork::ConnectionMadeNoQOCInfo


## -description


The 
<b>ConnectionMadeNoQOCInfo</b> method notifies your application that the specified connection has been established with no Quality of Connection information available.
<div class="alert"><b>Note</b>  This method is only available for TCP/IP connections.</div><div> </div>

## -parameters




### -param bstrConnection [in]

For WAN connections, the information passed is the connection name. For WAN connections, the connection name is the name of the phone book entry. For LAN connections, the information passed is "LAN connection".


### -param ulType [in]

Connection type. This value can be CONNECTION_LAN (0) or CONNECTION_WAN (1).


## -returns



This method can return one of these values.

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
Method returned successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify your application that the specified connection has been established when Quality of Connection information is not available.


			Filtering can be performed on the publisher property <i>ulConnectionMadeTypeNoQOC</i> by setting it to either CONNECTION_LAN or CONNECTION_WAN or both. Use 
<a href="_cos_ieventsubscription_putpublisherproperty">IEventSubscription::PutPublisherProperty</a> to set the publisher property.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="_cos_ieventsubscription">IEventSubscription</a>



<a href="_cos_ieventsubscription_putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/1cea5dff-13ea-4afb-84ac-7b8df4f55fc8">ISensNetwork</a>



<a href="https://msdn.microsoft.com/3b067a6f-ba4c-4914-aa5b-e0fd7690e75c">ISensNetwork::ConnectionMade</a>
 

 

