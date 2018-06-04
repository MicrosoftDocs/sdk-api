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

# IDMOWrapperFilter interface


## -description



The <code>IDMOWrapperFilter</code> interface enables an application to use a DirectX Media Object (DMO) inside a filter graph. The <a href="https://msdn.microsoft.com/ffa6234d-9040-4838-8f51-0cf87df40a5c">DMO Wrapper</a> filter exposes this interface.

To add a DMO to the filter graph, create an instance of the DMO Wrapper filter and query it for the <code>IDMOWrapperFilter</code> interface. Then call the <a href="https://msdn.microsoft.com/45f305b5-82bc-44c1-9af7-93aab371ed33">IDMOWrapperFilter::Init</a> method to initialize the filter with the DMO.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDMOWrapperFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDMOWrapperFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMOWrapperFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes the DMO Wrapper filter with the specified DMO.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e4424740-31b9-4317-8791-6a9aebb0c7e6">DirectX Media Objects</a>
 

 

