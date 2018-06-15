---
UID: NN:tuner.IComponentTypes
title: IComponentTypes
author: windows-sdk-content
description: The IComponentTypes interface is implemented on ComponentTypes objects and contains methods that enable applications to enumerate, add, remove and retrieve individual ComponentType objects. All ComponentTypes objects also support IPersistPropertyBag.
old-location: mstv\icomponenttypes.htm
old-project: mstv
ms.assetid: 47c3837b-1348-4359-ad3d-3d82c5fe3781
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IComponentTypes, IComponentTypes interface [Microsoft TV Technologies], IComponentTypes interface [Microsoft TV Technologies],described, IComponentTypesInterface, mstv.icomponenttypes, tuner/IComponentTypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponentTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentTypes interface


## -description



The <b>IComponentTypes</b> interface is implemented on <a href="https://msdn.microsoft.com/b0a468fd-6294-4148-a727-3a4bd51df6dc">ComponentTypes</a> objects and contains methods that enable applications to enumerate, add, remove and retrieve individual <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> objects. All ComponentTypes objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentTypes</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponentTypes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponentTypes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a new <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c070998c-4350-4630-80c0-e3db46154845">EnumComponentTypes</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/ad7fb66d-6592-47ae-9a2f-4432d8aaaebb">IEnumComponentTypes</a> enumerator for all component types in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32ff7c56-3173-4aba-9884-6e388a41192d">get__NewEnum</a>
</td>
<td align="left" width="63%">
Enumeration method to support For...Each loops in Automation clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f353702-1be1-4fa0-9312-f76f23f63a2b">get_Count</a>
</td>
<td align="left" width="63%">
Returns the number of Component Types in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be2e6f1b-a9af-4c19-ae25-a096ceee96fc">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface pointer at the specified index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f38e844-d197-40c1-8715-ffe406274b3c">put_Item</a>
</td>
<td align="left" width="63%">
Replaces the <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> object at the specified index with a new ComponentType object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> object at the specified index number.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponentTypes)</code>.




## -see-also




<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

