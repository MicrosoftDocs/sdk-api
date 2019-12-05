---
UID: NN:propidl.IEnumSTATPROPSTG
title: IEnumSTATPROPSTG (propidl.h)
description: Iterates through an array of STATPROPSTG structures. The STATPROPSTG structures contain statistical data about properties in a property set.
old-location: stg\ienumstatpropstg.htm
tech.root: Stg
ms.assetid: e625e52a-5628-4d18-9282-aa1c141c83af
ms.date: 12/05/2018
ms.keywords: IEnumSTATPROPSTG, IEnumSTATPROPSTG interface [Structured Storage], IEnumSTATPROPSTG interface [Structured Storage],described, _stg_ienumstatpropstg, propidlbase/IEnumSTATPROPSTG, stg.ienumstatpropstg
ms.topic: interface
f1_keywords:
- propidl/IEnumSTATPROPSTG
dev_langs:
- c++
req.header: propidl.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IEnumSTATPROPSTG
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATPROPSTG interface


## -description


The 
<b>IEnumSTATPROPSTG</b> interface iterates through an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structures. The <b>STATPROPSTG</b> structures contain statistical data about properties in a property set. <b>IEnumSTATPROPSTG</b> has the same methods as all enumerator interfaces: <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-next">Next</a>, <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-skip">Skip</a>, <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-reset">Reset</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-clone">Clone</a>.

The implementation defines the order in which the properties in the set are enumerated. Properties that are present when the enumerator is created, and are not removed during the enumeration, will be enumerated only once. Properties added or deleted while the enumeration is in progress may or may not be enumerated, but will never be enumerated more than once.


<a href="https://docs.microsoft.com/windows/desktop/Stg/reserved-property-identifiers">Reserved property identifiers</a>, properties with a property ID of 0 (dictionary), 1 (code page indicator), or greater than or equal to 0x80000000 are not enumerated.

Enumeration of a nonsimple property does not necessarily indicate that the property can be read successfully through a call to <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">IPropertyStorage::ReadMultiple</a>. This is because the performance overhead of checking existence of the indirect stream or storage is prohibitive during property enumeration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATPROPSTG</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSTATPROPSTG</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSTATPROPSTG</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structure enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-next">Next</a>
</td>
<td align="left" width="63%">
Gets a specified number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning of the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structure array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structures in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">IPropertyStorage::Enum</a>
 

 

