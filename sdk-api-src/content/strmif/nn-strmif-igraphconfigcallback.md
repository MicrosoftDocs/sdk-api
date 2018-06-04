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

# IGraphConfigCallback interface


## -description



The <code>IGraphConfigCallback</code> interface contains the callback method passed to <a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">IGraphConfig::Reconfigure</a>. The caller (an application or filter) implements this interface. For more information, see <a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphConfigCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGraphConfigCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGraphConfigCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4f44639-b3b0-412e-8b71-e1f994dee0e6">Reconfigure</a>
</td>
<td align="left" width="63%">
Callback method passed to <a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">IGraphConfig::Reconfigure</a>.

</td>
</tr>
</table> 

