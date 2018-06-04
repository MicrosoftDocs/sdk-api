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

# IComponent interface


## -description



The <b>IComponent</b> interface a base class for all derived interfaces such as <a href="https://msdn.microsoft.com/63d1ae17-8e38-457e-98d7-e81e7576f1c1">IMPEG2Component</a> and it describes the general characteristics of a component, which is an elementary stream within the program stream. The derived interfaces describe the properties of a component that are specific to a given network type. Component objects are created and attached to the tune request by the BDA Transport Information Filter (TIF) after reception has begun. All component objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IComponent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c041173-0c78-486e-93b5-a46c9dc0afb1">get_DescLangID</a>
</td>
<td align="left" width="63%">
Retrieves the language for presentation of the description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef7d1308-27ff-4d4d-b88d-58a9f89abc7f">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the description of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f517db8-a207-472e-8c6c-7cb2cac91f62">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the requested or actual status of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19eb345f-24a2-4522-87cc-fc4953faf343">get_Type</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface describing the general characteristics of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f914835-e097-4a02-80fe-371154c9d95a">put_DescLangID</a>
</td>
<td align="left" width="63%">
Sets the language for presentation of the description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e45ea3ea-e9e2-41f9-b171-bc95aa5cc590">put_Description</a>
</td>
<td align="left" width="63%">
Sets the description of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1f9cf98-69fd-4c54-8023-742f86413220">put_Status</a>
</td>
<td align="left" width="63%">
Sets the requested or actual status of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07d8cc28-d34e-4332-8648-d69a471ca8ac">put_Type</a>
</td>
<td align="left" width="63%">
Sets an <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> object describing the general characteristics of the Component.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponent)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

