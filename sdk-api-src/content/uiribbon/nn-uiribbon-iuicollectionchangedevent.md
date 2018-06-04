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

# IUICollectionChangedEvent interface


## -description


The <b>IUICollectionChangedEvent</b> interface is 
		implemented by the application and defines the method required to handle changes 
		to a collection at run time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUICollectionChangedEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUICollectionChangedEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUICollectionChangedEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265394">OnChanged</a>
</td>
<td align="left" width="63%">
Called when an <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a> changes.

</td>
</tr>
</table> 


## -remarks



The Windows Ribbon framework incorporates the standard Component Object Model (COM)  client-server mechanism of <a href="http://go.microsoft.com/fwlink/p/?linkid=132598">connectable objects</a> to listen for and handle collection changed events at run time.

The Ribbon acts as the COM server connectable object that defines both incoming and outgoing notification interfaces for the client, which is the Ribbon host application. The incoming interfaces are implemented by the Ribbon. The  outgoing interfaces are implemented by the application in a dedicated object that is created by the application and  referred to as the client connection sink. This sink is used to establish a connection to the connectable object.

In addition to defining the incoming and outgoing interfaces, the Ribbon must also implement the <a href="http://go.microsoft.com/fwlink/p/?linkid=144035">IConnectionPointContainer</a> interface and  create at least one connection point object that implements the <a href="http://go.microsoft.com/fwlink/p/?linkid=144038">IConnectionPoint</a> interface and manages the connection with the client sink.

<div class="alert"><b>Note</b>  The client must query the connectable object for <a href="http://go.microsoft.com/fwlink/p/?linkid=144035">IConnectionPointContainer</a> to determine whether the object is connectable before the client attempts to create a sink object.</div>
<div> </div>
In the case of the Ribbon,  <b>IUICollectionChangedEvent</b> is the outgoing interface defined by the framework and implemented by the application. The Ribbon triggers the <a href="https://msdn.microsoft.com/5a524071-2679-44c7-85db-a40cfcb4a321">IUICollectionChangedEvent::OnChanged</a> event in the client by sending an outgoing notification when a collection changes, for example, adding a Command to the Quick Access Toolbar (QAT).




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=132598">Events in COM and Connectable Objects</a>



<a href="https://msdn.microsoft.com/1a462f4e-e75a-40cf-9c52-0bad0a645d57">Gallery Sample</a>



<a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>
 

 

