---
UID: NN:webapplication.IWebApplicationHost
title: IWebApplicationHost (webapplication.h)
author: windows-sdk-content
description: Exposes methods and properties that are implemented by the WWAHost.
old-location: debug\iwebapplicationhost.htm
tech.root: debug_wwahost
ms.assetid: ac0ace8e-3f83-44be-baee-560c5472aa08
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWebApplicationHost, IWebApplicationHost interface [Debugging Windows Store apps], IWebApplicationHost interface [Debugging Windows Store apps],described, debug.iwebapplicationhost, webapplication/IWebApplicationHost
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
 - IWebApplicationHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWebApplicationHost interface


## -description


Exposes methods and properties that are implemented by the WWAHost.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWebApplicationHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWebApplicationHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-advise">Advise</a>
</td>
<td align="left" width="63%">
Establishes a connection to allow a client to receive events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the current document without sending a 'Pragma:no-cache' HTTP header to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Removes a previously established connection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationHost</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-document">Document</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the HTML document object model of the current top-level document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-hwnd">HWND</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the handle of the current WWAHost window.

</td>
</tr>
</table> 

