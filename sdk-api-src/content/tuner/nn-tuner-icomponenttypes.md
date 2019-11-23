---
UID: NN:tuner.IComponentTypes
title: IComponentTypes (tuner.h)

description: The IComponentTypes interface is implemented on ComponentTypes objects and contains methods that enable applications to enumerate, add, remove and retrieve individual ComponentType objects. All ComponentTypes objects also support IPersistPropertyBag.
old-location: mstv\icomponenttypes.htm
tech.root: mstv
ms.assetid: 47c3837b-1348-4359-ad3d-3d82c5fe3781

ms.date: 12/05/2018
ms.keywords: IComponentTypes, IComponentTypes interface [Microsoft TV Technologies], IComponentTypes interface [Microsoft TV Technologies],described, IComponentTypesInterface, mstv.icomponenttypes, tuner/IComponentTypes
ms.topic: interface
f1_keywords: 
 - "tuner/IComponentTypes"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponentTypes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentTypes interface


## -description



The <b>IComponentTypes</b> interface is implemented on <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/componenttypes-object">ComponentTypes</a> objects and contains methods that enable applications to enumerate, add, remove and retrieve individual <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects. All ComponentTypes objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentTypes</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponentTypes</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-add">Add</a>
</td>
<td align="left" width="63%">
Adds a new <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-enumcomponenttypes">EnumComponentTypes</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponenttypes">IEnumComponentTypes</a> enumerator for all component types in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Enumeration method to support For...Each loops in Automation clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Returns the number of Component Types in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface pointer at the specified index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-put_item">put_Item</a>
</td>
<td align="left" width="63%">
Replaces the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> object at the specified index with a new ComponentType object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> object at the specified index number.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponentTypes)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

