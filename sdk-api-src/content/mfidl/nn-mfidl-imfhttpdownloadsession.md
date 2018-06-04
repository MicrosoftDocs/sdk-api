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

# IMFHttpDownloadSession interface


## -description


Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. Applications provide the <b>IMFHttpDownloadSession</b> interface to Media Foundation through the <a href="https://msdn.microsoft.com/D9DAE789-1C0E-42B4-87B6-593D3B67FE1F">CreateHttpDownloadSession</a> method on the <a href="https://msdn.microsoft.com/4A3A96FB-A7C5-40BB-AB8F-12A7F00FDCD1">IMFHttpDownloadSessionProvider</a> interface. Microsoft Media Foundation uses this interface to perform a “streaming”, or “progressive”, download of a resource identified by a HTTP or HTTPS URL. Multiple HTTP requests may be sent to download the resource. The <b>IMFHttpDownloadSession</b> interface is used to create these individual HTTP requests.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFHttpDownloadSession</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFHttpDownloadSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFHttpDownloadSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to specify that no more HTTP requests will be created, and allows <b>IMFHttpDownloadSession</b> to free any internal resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/111A075A-82A7-4607-9359-37B2DA97AFC5">CreateRequest</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to create an object that implements the <a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a> interface, which is used to send a single HTTP, or HTTPS request. Since multiple requests may be needed to fully download a resource, Media Foundation may invoke <b>CreateRequest</b> multiple times on the same <b>IMFHttpDownloadSession</b> instance. Media Foundation will use each <b>IMFHttpDownloadRequest</b> instance for only a single request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/408D4863-D95F-4BBD-9F0B-9796ED08A256">SetServer</a>
</td>
<td align="left" width="63%">
Called  by Microsoft Media Foundation to specify parameters common to all requests created by this instance of <b>IMFHttpDownloadSession</b>.

</td>
</tr>
</table> 

