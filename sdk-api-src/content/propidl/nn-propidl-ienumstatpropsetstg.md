---
UID: NN:propidl.IEnumSTATPROPSETSTG
title: IEnumSTATPROPSETSTG
author: windows-sdk-content
description: Iterates through an array of STATPROPSETSTG structures. The STATPROPSETSTG structures contain statistical data about the property sets managed by the current IPropertySetStorage instance.
old-location: stg\ienumstatpropsetstg.htm
old-project: Stg
ms.assetid: 8d5e658f-312c-4c91-8794-808b2e8dd182
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumSTATPROPSETSTG, IEnumSTATPROPSETSTG interface [Structured Storage], IEnumSTATPROPSETSTG interface [Structured Storage],described, _stg_ienumstatpropsetstg, propidlbase/IEnumSTATPROPSETSTG, stg.ienumstatpropsetstg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propidl.h
req.include-header: Propidl.h
req.redist: 
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
tech.root: 
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
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
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IEnumSTATPROPSETSTG interface


## -description


The 
<b>IEnumSTATPROPSETSTG</b> interface iterates through an array of 
<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures. The <b>STATPROPSETSTG</b> structures contain statistical data about the property sets managed by the current <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> instance. <b>IEnumSTATPROPSETSTG</b> has the same methods as all enumerator interfaces: <a href="https://msdn.microsoft.com/3af3c518-3db4-4436-b1c1-86587ce8fbf3">Next</a>, <a href="https://msdn.microsoft.com/48275ca5-f9d1-42cb-b218-f51488a91bf8">Skip</a>, <a href="https://msdn.microsoft.com/41207be6-81ec-4dfc-a737-eb56792edb6d">Reset</a>, and 
<a href="https://msdn.microsoft.com/f875d5e9-fac0-4961-9570-342f55cf307e">Clone</a>.

The implementation defines the order in which the property sets are enumerated. Property sets that are present when the enumerator is created, and are not removed during the enumeration, will be enumerated only once. Property sets added or deleted while the enumeration is in progress may or may not be enumerated, but, if enumerated, will not be enumerated more than once.

For more information about how the COM compound document implementation of <a href="https://msdn.microsoft.com/3af3c518-3db4-4436-b1c1-86587ce8fbf3">IEnumSTATPROPSETSTG::Next</a> supplies members of the 
<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structure, see <a href="https://msdn.microsoft.com/1ce36e40-518c-411b-be5a-835a2dd0995e">IEnumSTATPROPSETSTG--Compound File Implementation</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATPROPSETSTG</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSTATPROPSETSTG</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f875d5e9-fac0-4961-9570-342f55cf307e">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the current <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structure enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3af3c518-3db4-4436-b1c1-86587ce8fbf3">Next</a>
</td>
<td align="left" width="63%">
Gets a specified number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41207be6-81ec-4dfc-a737-eb56792edb6d">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning of the <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structure array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48275ca5-f9d1-42cb-b218-f51488a91bf8">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">IPropertyStorage::Enum</a>
 

 

