---
UID: NN:webapplication.IWebApplicationUpdateEvents
title: IWebApplicationUpdateEvents (webapplication.h)

description: Enables an authoring app to receive notification of designer events and respond to those events.
old-location: debug\iwebapplicationupdateevents.htm
tech.root: debug_wwahost
ms.assetid: C1ED87B6-CC24-48CF-BC9F-FF702A0903E8

ms.date: 12/05/2018
ms.keywords: IWebApplicationUpdateEvents, IWebApplicationUpdateEvents interface [Debugging Windows Store apps], IWebApplicationUpdateEvents interface [Debugging Windows Store apps],described, debug.iwebapplicationupdateevents, webapplication/IWebApplicationUpdateEvents
ms.topic: interface
f1_keywords: 
 - "webapplication/IWebApplicationUpdateEvents"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWebApplicationUpdateEvents interface


## -description


Enables an authoring app to receive notification of designer events and respond to those events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebApplicationUpdateEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWebApplicationUpdateEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationupdateevents-oncsschanged">OnCssChanged</a>
</td>
<td align="left" width="63%">
Notifies the authoring app that the CSS has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationupdateevents-onpaint">OnPaint</a>
</td>
<td align="left" width="63%">
Notifies the authoring app that a portion of the app was painted.

</td>
</tr>
</table> 

