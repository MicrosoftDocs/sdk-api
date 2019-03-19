---
UID: NN:webapplication.IWebApplicationUpdateEvents
title: IWebApplicationUpdateEvents (webapplication.h)
author: windows-sdk-content
description: Enables an authoring app to receive notification of designer events and respond to those events.
old-location: debug\iwebapplicationupdateevents.htm
tech.root: debug_wwahost
ms.assetid: C1ED87B6-CC24-48CF-BC9F-FF702A0903E8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWebApplicationUpdateEvents, IWebApplicationUpdateEvents interface [Debugging Windows Store apps], IWebApplicationUpdateEvents interface [Debugging Windows Store apps],described, debug.iwebapplicationupdateevents, webapplication/IWebApplicationUpdateEvents
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
 - IWebApplicationUpdateEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebApplicationUpdateEvents interface


## -description


Enables an authoring app to receive notification of designer events and respond to those events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationUpdateEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWebApplicationUpdateEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWebApplicationUpdateEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8C959152-3576-4131-BD32-5777F1F570A1">OnCssChanged</a>
</td>
<td align="left" width="63%">
Notifies the authoring app that the CSS has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DFFED801-CCE7-4408-BD0B-E2B1AF5CD172">OnPaint</a>
</td>
<td align="left" width="63%">
Notifies the authoring app that a portion of the app was painted.

</td>
</tr>
</table> 

