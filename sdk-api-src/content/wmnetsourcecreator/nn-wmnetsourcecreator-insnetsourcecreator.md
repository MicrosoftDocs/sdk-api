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

# INSNetSourceCreator interface


## -description



The <b>INSNetSourceCreator</b> interface creates an administrative network source <a href="wmformat_glossary.htm">plug-in</a>. You can use an administrative network source plug-in to cache passwords and to locate the appropriate proxy server to use for Internet operations.

To get a pointer to the <b>INSNetSourceCreator</b> interface, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with <b>CLSID_ClientNetManager</b> as the <i>REFCLSID</i> parameter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INSNetSourceCreator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INSNetSourceCreator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INSNetSourceCreator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CreateNetSource</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/147b431f-84ed-40b9-85a8-3c220b56cd3f">GetNetSourceAdminInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an administrative network source object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetNetSourceProperties</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetNetSourceSharedNamespace</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetNumProtocolsSupported</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetProtocolName</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the network source creator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the network source creator.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

