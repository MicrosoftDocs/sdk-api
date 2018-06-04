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

# IWebApplicationNavigationEvents interface


## -description


Enables a debugging or authoring app to receive notification of navigation events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationNavigationEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWebApplicationNavigationEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWebApplicationNavigationEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1088bfa3-0a20-4156-90ff-50129e903052">BeforeNavigate</a>
</td>
<td align="left" width="63%">
Fired before navigate occurs in the given host (window or frameset element).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18dabd8a-d35c-4095-985d-bf712c539df8">DocumentComplete</a>
</td>
<td align="left" width="63%">
Fired when the document being navigated to reaches ReadyState_Complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f38f6d2-19a3-4c19-9670-7fd766b90bd3">DownloadBegin</a>
</td>
<td align="left" width="63%">
Download of a page has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a787ae3b-060a-4a7e-b980-e33d3d6b2a01">DownloadComplete</a>
</td>
<td align="left" width="63%">
Download of a page has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a80227-69ec-4f12-8d19-d2b932fbbfc0">NavigateComplete</a>
</td>
<td align="left" width="63%">
Fired when the document being navigated to becomes visible and enters the navigation stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c6e34e8-e14f-4b6c-ad83-140a7141cf64">NavigateError</a>
</td>
<td align="left" width="63%">
Fired when a binding error occurs (window or frameset element).

</td>
</tr>
</table> 

