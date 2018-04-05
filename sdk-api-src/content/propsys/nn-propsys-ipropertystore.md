---
UID: NN:propsys.IPropertyStore
title: IPropertyStore
author: windows-driver-content
description: Exposes methods for enumerating, getting, and setting property values.
old-location: properties\IPropertyStore.htm
old-project: properties
ms.assetid: e995aaa1-d4c9-475f-b1fa-b9123cd5b653
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IPropertyStore, IPropertyStore interface [Windows Properties], IPropertyStore interface [Windows Properties], described, properties.IPropertyStore, propsys/IPropertyStore, shell.IPropertyStore, shell_IPropertyStore, shell_IPropertyStore_cpp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyStore
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPropertyStore interface


## -description


Exposes methods for enumerating, getting, and setting property values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Saves a property change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">
Gets a property key from an item's array of properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of properties attached to the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Gets data for a specific property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>
</td>
<td align="left" width="63%">
Sets a new property value, or replaces or removes an existing value.

</td>
</tr>
</table> 


## -remarks



These methods can be called at any time after initialization of the property handler but before property changes are written to the file through <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a>. At any other time, these methods return E_FAIL.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided by CLSID_InMemoryPropertyStore, as <a href="shell.IPropertyStoreCache">IPropertyStoreCache</a>. Users should never need to implement it themselves.

                

CLSID_InMemoryPropertyStore implements <a href="shell.IPropertyStoreCache">IPropertyStoreCache</a> instead of <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> so that it can store additional state information (<a href="shell.PSC_STATE">PSC_STATE</a>) about each of the properties in the cache. This information can be useful for property handler implementers. It can also be useful in other scenarios where a cache of property values is needed.



