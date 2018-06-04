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

# IWbemQuery interface


## -description


The 
<b>IWbemQuery</b> interface provides an entry point through which a <a href="gloss_w.htm">WMI Query Language</a> (WQL) query can be parsed. For more information about WQL, see <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL (SQL for WMI</a>).

The following table lists the methods for 
<b>IWbemQuery</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemQuery</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f6542e-2aab-40c1-81d5-d08b54b8aa40">Empty</a>
</td>
<td align="left" width="63%">
Frees the memory that the parser is holding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbc4329d-73b8-4104-b3e0-e6dc12938b4f">FreeMemory</a>
</td>
<td align="left" width="63%">
Frees the memory that the parser returned to the caller in the previous call to 
<a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">GetAnalysis</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">GetAnalysis</a>
</td>
<td align="left" width="63%">
Gets the results of a successfully parsed query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetQueryInfo</b></td>
<td align="left" width="63%">
Not implemented. Returns <b>E_NOTIMPL</b> if called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/372b004f-322e-459c-8db0-150b0483aa34">Parse</a>
</td>
<td align="left" width="63%">
Parses a query string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>SetLanguageFeatures</b></td>
<td align="left" width="63%">
Not implemented. Returns <b>E_NOTIMPL</b> if called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>TestLanguageFeatures</b></td>
<td align="left" width="63%">
Not implemented. Returns <b>E_NOTIMPL</b> if called.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a>
 

 

