---
UID: NN:propsys.IPersistSerializedPropStorage2
title: IPersistSerializedPropStorage2
author: windows-sdk-content
description: Exposes methods to persist serialized property storage data for later use and to restore persisted data to a new property store instance.
old-location: shell\IPersistSerializedPropStorage2.htm
tech.root: shell
ms.assetid: 7483b51e-d71d-4570-8b76-64e344c2227e
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IPersistSerializedPropStorage2, IPersistSerializedPropStorage2 interface [Windows Shell], IPersistSerializedPropStorage2 interface [Windows Shell],described, _shell_IPersistSerializedPropStorage2, propsys/IPersistSerializedPropStorage2, shell.IPersistSerializedPropStorage2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.dll
api_name:
 - IPersistSerializedPropStorage2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistSerializedPropStorage2 interface


## -description


Exposes methods to persist serialized property storage data for later use and to restore persisted data to a new property store instance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistSerializedPropStorage2</b> interface inherits from <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a>. <b>IPersistSerializedPropStorage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistSerializedPropStorage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5f349e4-227e-4023-ab80-e8f9fb94dabf">GetPropertyStorageBuffer</a>
</td>
<td align="left" width="63%">
Gets the serialized property storage buffer from the property store instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90fe3148-457e-4d29-a117-b0b0e0df92c4">GetPropertyStorageSize</a>
</td>
<td align="left" width="63%">
Gets the size of serialized property storage data from the property store instance.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8">IPersistSerializedPropStorage</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IPersistSerializedPropStorage2</b> is not intended for custom implementation. Use the system-provided implementation associated with the in-memory property store.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The in-memory property store, created by calling <a href="https://msdn.microsoft.com/6e7a2ac0-2a4a-41ec-a2a8-ddbe8aa45bc9">PSCreateMemoryPropertyStore</a>, provides an implementation of this interface. Use this implementation when you want to persist or restore serialized property storage data.



