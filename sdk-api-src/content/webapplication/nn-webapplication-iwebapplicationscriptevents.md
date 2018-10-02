---
UID: NN:webapplication.IWebApplicationScriptEvents
title: IWebApplicationScriptEvents
author: windows-sdk-content
description: Enables a debugging or authoring app to receive notification of scripting engine events.
old-location: debug\iwebapplicationscriptevents.htm
tech.root: debug_wwahost
ms.assetid: a33f99a0-7c2d-45df-8a6a-d3257d537c9b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWebApplicationScriptEvents, IWebApplicationScriptEvents interface [Debugging Windows Store apps], IWebApplicationScriptEvents interface [Debugging Windows Store apps],described, debug.iwebapplicationscriptevents, webapplication/IWebApplicationScriptEvents
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
 - IWebApplicationScriptEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebApplicationScriptEvents interface


## -description


Enables a debugging or authoring app to receive notification of scripting engine events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationScriptEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWebApplicationScriptEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWebApplicationScriptEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfb3cc08-e166-455a-b26b-e6f36b394df0">BeforeScriptExecuted</a>
</td>
<td align="left" width="63%">
Fired before any script is executed on the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f1e6260-804d-4881-b2d8-70a1463a46bd">ScriptError</a>
</td>
<td align="left" width="63%">
Fired when an unhandled script error occurs.

</td>
</tr>
</table> 

