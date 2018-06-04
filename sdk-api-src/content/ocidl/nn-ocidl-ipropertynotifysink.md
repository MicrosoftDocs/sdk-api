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

# IPropertyNotifySink interface


## -description


Implemented by a sink object to receive notifications about property changes from an object that supports <b>IPropertyNotifySink</b> as an outgoing interface. The client that needs to receive the notifications in this interface (from a supporting connectable object) creates a sink with this interface and connects it to the connectable object through the connection point mechanism. For more information on connection points, see <a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyNotifySink</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPropertyNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyNotifySink</b> interface has these methods.
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
Notifies a sink that a <a href="https://msdn.microsoft.com/ba09096d-a2f7-4958-827c-0fba19ded26f">bindable</a> property has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52f4c45d-d658-4de2-a494-2ae164604681">OnRequestEdit</a>
</td>
<td align="left" width="63%">
Notifies a sink that a <a href="https://msdn.microsoft.com/63f38d83-596b-4031-bb6a-972374cd0c60">requestedit</a> property is about to change.

</td>
</tr>
</table> 


## -remarks



The object is itself required to call the methods of <b>IPropertyNotifySink</b> only for those properties marked with the [<a href="https://msdn.microsoft.com/ba09096d-a2f7-4958-827c-0fba19ded26f">bindable</a>] and [<a href="https://msdn.microsoft.com/63f38d83-596b-4031-bb6a-972374cd0c60">requestedit</a>] attributes in the object's type information. When the object changes a [<b>bindable</b>] property, it is required to call <a href="https://msdn.microsoft.com/71ab5206-5127-45f1-a2b5-3fbcc867d678">IPropertyNotifySink::OnChanged</a>. When the object is about to change a [<b>requestedit</b>] property, it must call <a href="https://msdn.microsoft.com/52f4c45d-d658-4de2-a494-2ae164604681">IPropertyNotifySink::OnRequestEdit</a> before changing the property and must also honor the action specified by the sink on return from this call.

The one exception to this rule is that no notifications are sent as a result of an object's initialization or loading procedures. At initialization time, it is assumed that all properties change and that all must be allowed to change. Notifications to this interface are therefore meaningful only in the context of a fully initialized/loaded object.




## -see-also




<a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>



<a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a>
 

 

