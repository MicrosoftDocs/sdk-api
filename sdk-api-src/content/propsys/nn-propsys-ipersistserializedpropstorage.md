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

# IPersistSerializedPropStorage interface


## -description


Exposes methods to persist serialized property storage data for later use and to restore persisted data to a new property store instance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistSerializedPropStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPersistSerializedPropStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistSerializedPropStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86a1d7ec-759a-4b8a-91e1-4cfa28a17b41">GetPropertyStorage</a>
</td>
<td align="left" width="63%">
Gets the serialized property storage data from the property store instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
Toggles the property store object between the read-only and read/write state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b6d14ba-3de3-493e-8551-0f3caa02f339">SetPropertyStorage</a>
</td>
<td align="left" width="63%">
Initializes the property store instance from the specified serialized property storage data.

</td>
</tr>
</table> 


## -remarks



Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface to read and write values from and to the property store.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The in-memory property store, created by calling <a href="https://msdn.microsoft.com/6e7a2ac0-2a4a-41ec-a2a8-ddbe8aa45bc9">PSCreateMemoryPropertyStore</a>, provides an implementation of this interface. Use this implementation when you want to persist or restore serialized property storage data.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IPersistSerializedPropStorage</b> is not intended for custom implementation. Use the system-provided implementation associated with the in-memory property store.



