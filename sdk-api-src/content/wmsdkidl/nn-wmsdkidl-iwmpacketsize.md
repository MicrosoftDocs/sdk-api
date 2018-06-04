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

# IWMPacketSize interface


## -description



The <b>IWMPacketSize</b> interface controls the maximum size of <a href="wmformat_glossary.htm">packets</a> in an ASF file. Its methods are used to control the size of <a href="wmformat_glossary.htm">UDP</a> datagrams when the content, live or on-demand, is streamed across a network.

An <b>IWMPacketSize</b> interface can be obtained for either a profile object, a reader object, or a synchronous reader object. You can obtain a pointer to <b>IWMPacketSize</b> by calling the <b>QueryInterface</b> method of any of the other interfaces in one of the supported objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPacketSize</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPacketSize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPacketSize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8410c524-9c27-48ac-9a48-c17cae782764">GetMaxPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum size of a packet in an ASF file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8230c08-e60f-454d-93a5-037685d6151c">SetMaxPacketSize</a>
</td>
<td align="left" width="63%">
Specifies the maximum size of a packet in an ASF file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

