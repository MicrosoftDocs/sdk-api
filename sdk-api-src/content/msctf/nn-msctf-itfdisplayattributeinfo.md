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

# ITfDisplayAttributeInfo interface


## -description


The <b>ITfDisplayAttributeInfo</b> interface is implemented by a text service to provide display attribute data. This interface is used by any component, most often an application, that must determine how text displays.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDisplayAttributeInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfDisplayAttributeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDisplayAttributeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32e28feb-1186-4848-a9d4-70b27f865d3c">GetAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains the display attribute data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Obtains the description string of the display attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5202bf19-ae24-44f4-98f0-1f9d64d383a6">GetGUID</a>
</td>
<td align="left" width="63%">
Obtains the GUID for the display attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the display attribute data to its default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e9a472c-7992-48fc-be47-993f6d53f043">SetAttributeInfo</a>
</td>
<td align="left" width="63%">
Sets the new attribute data.

</td>
</tr>
</table> 


## -remarks



An application obtains an instance of this interface by calling <a href="https://msdn.microsoft.com/41bc183f-013f-4e68-bb72-d9a30d5ea48e">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</a> or <a href="https://msdn.microsoft.com/db374ba3-8a65-4933-85cb-320c294d6041">IEnumTfDisplayAttributeInfo::Next</a>.

A text service supplies an instance of this interface in its <a href="https://msdn.microsoft.com/2081f1b4-45b4-43bd-ba20-392a5ad0a30e">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</a> method.




## -see-also




<a href="https://msdn.microsoft.com/db374ba3-8a65-4933-85cb-320c294d6041">IEnumTfDisplayAttributeInfo::Next
      </a>



<a href="https://msdn.microsoft.com/41bc183f-013f-4e68-bb72-d9a30d5ea48e">
        ITfDisplayAttributeMgr::GetDisplayAttributeInfo
      </a>



<a href="https://msdn.microsoft.com/2081f1b4-45b4-43bd-ba20-392a5ad0a30e">
        ITfDisplayAttributeProvider::GetDisplayAttributeInfo
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

