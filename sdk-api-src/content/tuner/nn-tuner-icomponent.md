---
UID: NN:tuner.IComponent
title: IComponent (tuner.h)
author: windows-sdk-content
description: The IComponent interface a base class for all derived interfaces such as IMPEG2Component and it describes the general characteristics of a component, which is an elementary stream within the program stream.
old-location: mstv\icomponent.htm
tech.root: mstv
ms.assetid: 516b30ba-4f55-49b7-8085-d436bf4a94e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComponent, IComponent interface [Microsoft TV Technologies], IComponent interface [Microsoft TV Technologies],described, IComponentInterface, mstv.icomponent, tuner/IComponent
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
 - IComponent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponent interface


## -description



The <b>IComponent</b> interface a base class for all derived interfaces such as <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component</a> and it describes the general characteristics of a component, which is an elementary stream within the program stream. The derived interfaces describe the properties of a component that are specific to a given network type. Component objects are created and attached to the tune request by the BDA Transport Information Filter (TIF) after reception has begun. All component objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_desclangid">get_DescLangID</a>
</td>
<td align="left" width="63%">
Retrieves the language for presentation of the description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_description">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the description of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_status">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the requested or actual status of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_type">get_Type</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface describing the general characteristics of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-put_desclangid">put_DescLangID</a>
</td>
<td align="left" width="63%">
Sets the language for presentation of the description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-put_description">put_Description</a>
</td>
<td align="left" width="63%">
Sets the description of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-put_status">put_Status</a>
</td>
<td align="left" width="63%">
Sets the requested or actual status of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-put_type">put_Type</a>
</td>
<td align="left" width="63%">
Sets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> object describing the general characteristics of the Component.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponent)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

