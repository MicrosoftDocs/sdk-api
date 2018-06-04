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

# IMFNetResourceFilter interface


## -description


Notifies the application when a byte stream requests a URL, and enables the application to block URL redirection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetResourceFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetResourceFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetResourceFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/418EA3E0-9732-43B7-BF80-A85ECB7A9485">OnRedirect</a>
</td>
<td align="left" width="63%">
Called when the byte stream redirects to a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4FE6BBE8-A8EC-4304-BC4B-4D49F8EADC25">OnSendingRequest</a>
</td>
<td align="left" width="63%">
Called when the byte stream requests a URL.

</td>
</tr>
</table> 


## -remarks



To set the callback interface:

<ol>
<li>Query the byte stream object for the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/da0c3d59-07c4-4431-a137-8655ddbf6258">IMFAttributes::SetUnknown</a> to set the <a href="https://msdn.microsoft.com/C035B4AD-CF99-4A4F-9384-F80A3620BD27">MFNETSOURCE_RESOURCE_FILTER</a> attribute.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

