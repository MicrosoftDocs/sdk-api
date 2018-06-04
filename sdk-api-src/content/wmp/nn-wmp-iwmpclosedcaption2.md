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

# IWMPClosedCaption2 interface


## -description



The <b>IWMPClosedCaption2</b> interface provides closed captioning methods that supplement the <b>IWMPClosedCaption</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPClosedCaption2</b> interface inherits from <a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption</a>. <b>IWMPClosedCaption2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPClosedCaption2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6de8bef5-f0d1-498b-a482-e3f1c3e53c24">get_SAMILangCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of languages supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e31985e3-e5ab-4a29-b0d7-9a1cda58bca1">get_SAMIStyleCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of styles supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c17418ce-d653-43b3-9702-62c049eecdfc">getSAMILangID</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2da5045-4000-46d8-a610-f5f80cb6f713">getSAMILangName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a language supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dfdbe70-2aa8-4cae-8886-6b770707652e">getSAMIStyleName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a style supported by the current SAMI file.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPClosedCaption2</b> interface by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption</a> interface.

	


## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

