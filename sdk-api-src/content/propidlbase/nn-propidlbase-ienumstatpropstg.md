---
UID: NN:propidlbase.IEnumSTATPROPSTG
title: IEnumSTATPROPSTG
author: windows-sdk-content
description: Iterates through an array of STATPROPSTG structures. The STATPROPSTG structures contain statistical data about properties in a property set.
old-location: stg\ienumstatpropstg.htm
old-project: stg
ms.assetid: e625e52a-5628-4d18-9282-aa1c141c83af
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IEnumSTATPROPSTG, IEnumSTATPROPSTG interface [Structured Storage], IEnumSTATPROPSTG interface [Structured Storage],described, _stg_ienumstatpropstg, propidlbase/IEnumSTATPROPSTG, stg.ienumstatpropstg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STATPROPSTG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATPROPSTG
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IEnumSTATPROPSTG interface


## -description



			The 
<b>IEnumSTATPROPSTG</b> interface iterates through an array of 
<a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures. The <b>STATPROPSTG</b> structures contain statistical data about properties in a property set. <b>IEnumSTATPROPSTG</b> has the same methods as all enumerator interfaces: <a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>, and 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>.

The implementation defines the order in which the properties in the set are enumerated. Properties that are present when the enumerator is created, and are not removed during the enumeration, will be enumerated only once. Properties added or deleted while the enumeration is in progress may or may not be enumerated, but will never be enumerated more than once.


<a href="https://msdn.microsoft.com/d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c">Reserved property identifiers</a>, properties with a property ID of 0 (dictionary), 1 (code page indicator), or greater than or equal to 0x80000000 are not enumerated.

Enumeration of a nonsimple property does not necessarily indicate that the property can be read successfully through a call to <a href="https://msdn.microsoft.com/a3d708fe-53af-4f1b-94ac-edc40d59a034">IPropertyStorage::ReadMultiple</a>. This is because the performance overhead of checking existence of the indirect stream or storage is prohibitive during property enumeration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATPROPSTG</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSTATPROPSTG</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structure enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Gets a specified number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning of the <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structure array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">IPropertyStorage::Enum</a>
 

 

