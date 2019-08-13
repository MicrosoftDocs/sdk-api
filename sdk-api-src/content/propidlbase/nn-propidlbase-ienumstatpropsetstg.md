---
UID: NN:propidlbase.IEnumSTATPROPSETSTG
title: IEnumSTATPROPSETSTG (propidlbase.h)
author: windows-sdk-content
description: Iterates through an array of STATPROPSETSTG structures. The STATPROPSETSTG structures contain statistical data about the property sets managed by the current IPropertySetStorage instance.
old-location: stg\ienumstatpropsetstg.htm
tech.root: Stg
ms.assetid: 8d5e658f-312c-4c91-8794-808b2e8dd182
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSTATPROPSETSTG, IEnumSTATPROPSETSTG interface [Structured Storage], IEnumSTATPROPSETSTG interface [Structured Storage],described, _stg_ienumstatpropsetstg, propidlbase/IEnumSTATPROPSETSTG, stg.ienumstatpropsetstg
ms.topic: interface
f1_keywords: 
 - "propidlbase/IEnumSTATPROPSETSTG"
req.header: propidlbase.h
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
 - IEnumSTATPROPSETSTG
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATPROPSETSTG interface


## -description


The 
<b>IEnumSTATPROPSETSTG</b> interface iterates through an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures. The <b>STATPROPSETSTG</b> structures contain statistical data about the property sets managed by the current <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> instance. <b>IEnumSTATPROPSETSTG</b> has the same methods as all enumerator interfaces: <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-next">Next</a>, <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-skip">Skip</a>, <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-reset">Reset</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-clone">Clone</a>.

The implementation defines the order in which the property sets are enumerated. Property sets that are present when the enumerator is created, and are not removed during the enumeration, will be enumerated only once. Property sets added or deleted while the enumeration is in progress may or may not be enumerated, but, if enumerated, will not be enumerated more than once.

For more information about how the COM compound document implementation of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-next">IEnumSTATPROPSETSTG::Next</a> supplies members of the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure, see <a href="https://docs.microsoft.com/windows/desktop/Stg/ienumstatpropsetstg-compound-file-implementation">IEnumSTATPROPSETSTG--Compound File Implementation</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATPROPSETSTG</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSTATPROPSETSTG</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSTATPROPSETSTG</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the current <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-next">Next</a>
</td>
<td align="left" width="63%">
Gets a specified number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning of the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">IPropertyStorage::Enum</a>
 

 

