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

# IDataRetrieverCallback interface


## -description


Represents methods that an <b>IAsynchronousDataRetriever</b> object can call to indicate that processing has been completed on an <b>IAsynchronousDataRetriever</b> method.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataRetrieverCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDataRetrieverCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataRetrieverCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b48f9a91-f211-4df4-b315-dfe8d48b3db7">LoadChangeDataComplete</a>
</td>
<td align="left" width="63%">
Indicates that <a href="https://msdn.microsoft.com/b5e73504-1f9e-4a58-9bd9-2c184372b970">IAsynchronousDataRetriever::LoadChangeData</a> has finished successfully.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93185b3d-458d-4254-af2d-02cf7b1c5be7">LoadChangeDataError</a>
</td>
<td align="left" width="63%">
Indicates that an <b>IAsynchronousDataRetriever</b> method failed.



</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

