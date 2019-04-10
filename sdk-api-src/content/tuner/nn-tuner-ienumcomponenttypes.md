---
UID: NN:tuner.IEnumComponentTypes
title: IEnumComponentTypes (tuner.h)
author: windows-sdk-content
description: The IEnumComponentTypes interface is implemented on a standard COM collection of ComponentType objects associated with a given broadcast stream, and returned through a call to IComponentTypes::EnumComponentTypes.
old-location: mstv\ienumcomponenttypes.htm
tech.root: mstv
ms.assetid: ad7fb66d-6592-47ae-9a2f-4432d8aaaebb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumComponentTypes, IEnumComponentTypes interface [Microsoft TV Technologies], IEnumComponentTypes interface [Microsoft TV Technologies],described, IEnumComponentTypesInterface, mstv.ienumcomponenttypes, tuner/IEnumComponentTypes
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
 - IEnumComponentTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumComponentTypes interface


## -description



The <b>IEnumComponentTypes</b> interface is implemented on a standard COM collection of <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> objects associated with a given broadcast stream, and returned through a call to <a href="https://msdn.microsoft.com/c070998c-4350-4630-80c0-e3db46154845">IComponentTypes::EnumComponentTypes</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumComponentTypes</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumComponentTypes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumComponentTypes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/777c7302-5b5b-4263-ad9e-3d1bff5328fc">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the entire collection and all its sub-objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/491e9237-38cd-4c12-b93b-eb398a49d742">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7eead32c-a02c-41c1-8cfb-a52180219697">Reset</a>
</td>
<td align="left" width="63%">
Moves the iterator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea6c0ff8-76ae-4783-9b99-154ecb210a17">Skip</a>
</td>
<td align="left" width="63%">
Skips the element at the specified index.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumComponentTypes)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

