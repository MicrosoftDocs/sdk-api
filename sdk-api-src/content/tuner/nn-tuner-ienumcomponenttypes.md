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
ms.custom: 19H1
---

# IEnumComponentTypes interface


## -description



The <b>IEnumComponentTypes</b> interface is implemented on a standard COM collection of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects associated with a given broadcast stream, and returned through a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-enumcomponenttypes">IComponentTypes::EnumComponentTypes</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumComponentTypes</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumComponentTypes</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponenttypes-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the entire collection and all its sub-objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponenttypes-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponenttypes-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves the iterator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponenttypes-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the element at the specified index.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumComponentTypes)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

