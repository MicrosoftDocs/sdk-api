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

# IMFHttpDownloadSessionProvider interface


## -description


Applications implement this interface in order to provide custom a custom HTTP or HTTPS download implementation. Use the <a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a> interface to register the provider. For more information, see <a href="https://msdn.microsoft.com/94e2a411-96b8-4506-8491-78f4f5f286ce">Using the Source Resolver</a>. Once registered, the Microsoft Media Foundation will invoke the <a href="https://msdn.microsoft.com/D9DAE789-1C0E-42B4-87B6-593D3B67FE1F">CreateHttpDownloadSession</a> method of the provider  implementation to open HTTP or HTTPS URLs instead of using the default implementation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFHttpDownloadSessionProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFHttpDownloadSessionProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFHttpDownloadSessionProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D9DAE789-1C0E-42B4-87B6-593D3B67FE1F">CreateHttpDownloadSession</a>
</td>
<td align="left" width="63%">
Called by the Microsoft Media Foundation to open HTTP or HTTPS URLs instead of using the default implementation.

</td>
</tr>
</table> 

