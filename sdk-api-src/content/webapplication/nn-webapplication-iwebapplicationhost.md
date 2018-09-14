---
UID: NN:webapplication.IWebApplicationHost
title: IWebApplicationHost
author: windows-sdk-content
description: Exposes methods and properties that are implemented by the WWAHost.
old-location: debug\iwebapplicationhost.htm
tech.root: debug_wwahost
ms.assetid: ac0ace8e-3f83-44be-baee-560c5472aa08
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWebApplicationHost, IWebApplicationHost interface [Debugging Windows Store apps], IWebApplicationHost interface [Debugging Windows Store apps],described, debug.iwebapplicationhost, webapplication/IWebApplicationHost
ms.prod: windows
ms.technology: windows-sdk
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
---

# IWebApplicationHost interface


## -description


Exposes methods and properties that are implemented by the WWAHost.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationHost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWebApplicationHost</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/94c016cb-f043-4ea6-a5d1-f3486b55c97f">Advise</a>
</td>
<td align="left" width="63%">
Establishes a connection to allow a client to receive events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f94cc9-9407-4844-a100-8144fc6f45ce">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the current document without sending a 'Pragma:no-cache' HTTP header to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daab1a3f-1f84-4559-bdc0-be8f1fb28904">Unadvise</a>
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

<a href="https://msdn.microsoft.com/e2ba8ea7-0179-42d6-8d85-1617d14f85e4">Document</a>


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

<a href="https://msdn.microsoft.com/7c013f82-6d1f-494d-9f7a-77c7ff72f0d4">HWND</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the handle of the current WWAHost window.

</td>
</tr>
</table> 

