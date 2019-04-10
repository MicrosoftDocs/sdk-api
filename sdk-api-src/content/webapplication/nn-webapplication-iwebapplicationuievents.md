---
UID: NN:webapplication.IWebApplicationUIEvents
title: IWebApplicationUIEvents (webapplication.h)
author: windows-sdk-content
description: Enables a debugging or authoring app to receive notification of user interface events and respond to events that require user interaction.
old-location: debug\iwebapplicationuievents.htm
tech.root: debug_wwahost
ms.assetid: e7cfc572-f727-41f4-b4a5-b15f3f3cd4e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWebApplicationUIEvents, IWebApplicationUIEvents interface [Debugging Windows Store apps], IWebApplicationUIEvents interface [Debugging Windows Store apps],described, debug.iwebapplicationuievents, webapplication/IWebApplicationUIEvents
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
 - IWebApplicationUIEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebApplicationUIEvents interface


## -description


Enables a debugging or authoring app to receive notification of user interface events and respond to events that require user interaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationUIEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWebApplicationUIEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWebApplicationUIEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3579ffe7-914c-4baf-b1bf-4ed1a1db645f">SecurityProblem</a>
</td>
<td align="left" width="63%">
Notifies the authoring app about an authentication problem.

</td>
</tr>
</table> 

