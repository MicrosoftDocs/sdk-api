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

# ITfReadOnlyProperty interface


## -description


The <b>ITfReadOnlyProperty</b> interface is implemented by the TSF manager and used by an application or text service to obtain property data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReadOnlyProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfReadOnlyProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfReadOnlyProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/201c518b-f06f-4c4f-aa56-f8d21f477814">EnumRanges</a>
</td>
<td align="left" width="63%">
Obtains an enumeration of ranges that contain unique values of the property within the given range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff545736">GetContext</a>
</td>
<td align="left" width="63%">
Obtains the context object for the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Obtains the property identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Obtains the value of the property for a range of text.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is obtained by using <a href="https://msdn.microsoft.com/5c04ff8e-5686-4802-b312-71dddaf0155e">ITfContext::GetAppProperty</a> or <a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">ITfContext::TrackProperties</a>.




## -see-also




<a href="https://msdn.microsoft.com/5c04ff8e-5686-4802-b312-71dddaf0155e">ITfContext::GetAppProperty
      </a>



<a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">
        ITfContext::TrackProperties
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

