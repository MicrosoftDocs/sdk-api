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

# ITfLMLattice interface


## -description


The <b>ITfLMLattice</b> interface is implemented by the speech text service to provide information about lattice element properties and is used by a client (application or other text service). A client obtains this interface from the GUID_PROP_LMLATTICE property by calling <a href="https://msdn.microsoft.com/c82ef360-e0b1-4e1a-b839-36b8e9c52347">ITfReadOnlyProperty::GetValue</a>. For more information, see <a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">Predefined Properties</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLMLattice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLMLattice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLMLattice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42ad69f-d27a-40b7-8d63-3b422cb69db5">EnumLatticeElements</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all lattice elements contained in the lattice property that start at or after a specific offset from the start of the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/199032f7-b97f-4475-9ce3-9af952e13f12">QueryType</a>
</td>
<td align="left" width="63%">
Determines if a specific lattice element type is supported by the lattice property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c82ef360-e0b1-4e1a-b839-36b8e9c52347">ITfReadOnlyProperty::GetValue
      </a>



<a href="_COM_IUnknown">IUnknown</a>



<a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">
        Predefined Properties
      </a>
 

 

