---
UID: NN:webapplication.IWebApplicationNavigationEvents
title: IWebApplicationNavigationEvents (webapplication.h)
author: windows-sdk-content
description: Enables a debugging or authoring app to receive notification of navigation events.
old-location: debug\iwebapplicationnavigationevents.htm
tech.root: debug_wwahost
ms.assetid: 580d4b21-3a4b-4e0c-b0d1-25b4e4fb2b1b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWebApplicationNavigationEvents, IWebApplicationNavigationEvents interface [Debugging Windows Store apps], IWebApplicationNavigationEvents interface [Debugging Windows Store apps],described, debug.iwebapplicationnavigationevents, webapplication/IWebApplicationNavigationEvents
ms.topic: interface
f1_keywords: 
 - "webapplication/IWebApplicationNavigationEvents"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWebApplicationNavigationEvents interface


## -description


Enables a debugging or authoring app to receive notification of navigation events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationNavigationEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWebApplicationNavigationEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationnavigationevents-beforenavigate">BeforeNavigate</a>
</td>
<td align="left" width="63%">
Fired before navigate occurs in the given host (window or frameset element).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationnavigationevents-documentcomplete">DocumentComplete</a>
</td>
<td align="left" width="63%">
Fired when the document being navigated to reaches ReadyState_Complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationnavigationevents-downloadbegin">DownloadBegin</a>
</td>
<td align="left" width="63%">
Download of a page has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationnavigationevents-downloadcomplete">DownloadComplete</a>
</td>
<td align="left" width="63%">
Download of a page has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationnavigationevents-navigatecomplete">NavigateComplete</a>
</td>
<td align="left" width="63%">
Fired when the document being navigated to becomes visible and enters the navigation stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationnavigationevents-navigateerror">NavigateError</a>
</td>
<td align="left" width="63%">
Fired when a binding error occurs (window or frameset element).

</td>
</tr>
</table> 

