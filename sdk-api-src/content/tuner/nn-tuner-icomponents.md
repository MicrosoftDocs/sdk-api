---
UID: NN:tuner.IComponents
title: IComponents (tuner.h)
description: The IComponents interface represents a collection of components.helpviewer_keywords: ["IComponents","IComponents interface [Microsoft TV Technologies]","IComponents interface [Microsoft TV Technologies]","described","IComponentsInterface","mstv.icomponents","tuner/IComponents"]
old-location: mstv\icomponents.htm
tech.root: mstv
ms.assetid: 670b47ba-bcbd-4281-95e3-a5d784f0610b
ms.date: 12/05/2018
ms.keywords: IComponents, IComponents interface [Microsoft TV Technologies], IComponents interface [Microsoft TV Technologies],described, IComponentsInterface, mstv.icomponents, tuner/IComponents
f1_keywords:
- tuner/IComponents
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
- IComponents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponents interface


## -description



The <b>IComponents</b> interface represents a collection of components. In digital television, the term <i>component</i> refers to a substream within the program stream. For example, a program stream may have three audio streams in different languages; in this case each audio stream is a component of the program stream. The <b>IComponents</b> interface is implemented on the Components object, which is a collection of components. The Components object enables applications to enumerate components within a program stream and perform operations related to individual components in the collection. The Components object also supports <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponents</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-add">Add</a>
</td>
<td align="left" width="63%">
Adds a Component object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-enumcomponents">EnumComponents</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponents">IEnumComponents</a> enumerator for all components in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Enumeration method to support For…Each loops in Automation clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Gets the number of Component objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Enables the caller to access a component by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-put_item">put_Item</a>
</td>
<td align="left" width="63%">
Replaces an existing item in the collection with a new Component object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes a Component object from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponents)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

