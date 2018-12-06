---
UID: NN:webapplication.IWebApplicationNavigationEvents
title: IWebApplicationNavigationEvents
author: windows-sdk-content
description: Enables a debugging or authoring app to receive notification of navigation events.
old-location: debug\iwebapplicationnavigationevents.htm
tech.root: debug_wwahost
ms.assetid: 580d4b21-3a4b-4e0c-b0d1-25b4e4fb2b1b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWebApplicationNavigationEvents, IWebApplicationNavigationEvents interface [Debugging Windows Store apps], IWebApplicationNavigationEvents interface [Debugging Windows Store apps],described, debug.iwebapplicationnavigationevents, webapplication/IWebApplicationNavigationEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: webapplication.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Webapplication.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - webapplication.h
api_name:
 - IWebApplicationNavigationEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

