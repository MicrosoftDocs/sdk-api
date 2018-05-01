---
UID: NN:propsys.IPropertyChangeArray
title: IPropertyChangeArray
author: windows-driver-content
description: Exposes methods for several multiple change operations that may be passed to IFileOperation.
old-location: properties\IPropertyChangeArray.htm
old-project: properties
ms.assetid: c7de40d0-9fe6-4c4b-ba17-c4648501ce0a
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IPropertyChangeArray, IPropertyChangeArray interface [Windows Properties], IPropertyChangeArray interface [Windows Properties], described, _shell_IPropertyChangeArray, properties.IPropertyChangeArray, propsys/IPropertyChangeArray, shell.IPropertyChangeArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	IPropertyChangeArray
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyChangeArray interface


## -description


Exposes methods for several multiple change operations that may be passed to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyChangeArray</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyChangeArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyChangeArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyChangeArray_Append">Append</a>
</td>
<td align="left" width="63%">
Inserts a change operation at the end of an array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyChangeArray_AppendOrReplace">AppendOrReplace</a>
</td>
<td align="left" width="63%">
Replaces the first occurrence of a change that affects the same property key as the provided change.  If the property key is not already in the array, this method appends the change to the end of the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">
Gets the change operation at a specified array index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of change operations in the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyChangeArray_InsertAt">InsertAt</a>
</td>
<td align="left" width="63%">
Inserts a change operation into an array at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyChangeArray_IsKeyInArray">IsKeyInArray</a>
</td>
<td align="left" width="63%">
Specifies whether a particular property key exists in the change array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597596">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes a specified change.

</td>
</tr>
</table> 


## -remarks



Either call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with a class identifier (CLSID) of <b>CLSID_PropertyChangeArray</b> or call <a href="shell.PSCreatePropertyChangeArray">PSCreatePropertyChangeArray</a> to obtain a standard implementation of this interface. This is a container interface that allows multiple changes to be passed to a single file operation to prevent accessing a file multiple times.



