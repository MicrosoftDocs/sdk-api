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

# IPropertyNotifySink::OnRequestEdit


## -description


Notifies a sink that a <a href="https://msdn.microsoft.com/63f38d83-596b-4031-bb6a-972374cd0c60">requestedit</a> property is about to change.


## -parameters




### -param dispID [in]

The dispatch identifier of the property that is about to change or DISPID_UNKNOWN if multiple properties are about to change.


## -returns



This method can return the following values.

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
The specified property or properties are allowed to change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified property or properties are not allowed to change. The caller must obey this return value by discarding the new property value(s). This is part of the contract of the [<a href="https://msdn.microsoft.com/63f38d83-596b-4031-bb6a-972374cd0c60">requestedit</a>] attribute and this method.

</td>
</tr>
</table>
 




## -remarks



The sink may choose to allow or disallow the change to take place. For example, the sink may enforce a read-only state on the property. DISPID_UNKNOWN is a valid parameter to this method to indicate that multiple properties are about to change. In this case, the sink can enforce a global read-only state for all [<a href="https://msdn.microsoft.com/63f38d83-596b-4031-bb6a-972374cd0c60">requestedit</a>] properties in the object, including any specific ones that the sink otherwise recognizes.

If the sink allows changes, the object must also make <a href="https://msdn.microsoft.com/71ab5206-5127-45f1-a2b5-3fbcc867d678">IPropertyNotifySink::OnChanged</a> notifications for any properties that are marked [<a href="https://msdn.microsoft.com/ba09096d-a2f7-4958-827c-0fba19ded26f">bindable</a>] in addition to [<a href="https://msdn.microsoft.com/63f38d83-596b-4031-bb6a-972374cd0c60">requestedit</a>].



This method cannot be used to implement any sort of data validation. At the time of the call, the desired new value of the property is unavailable and thus cannot be validated. This method's only purpose is to allow the sink to enforce a read-only state on a property.




## -see-also




<a href="https://msdn.microsoft.com/bfdf315c-6375-4c77-abd8-03f07342820f">IPropertyNotifySink</a>
 

 

