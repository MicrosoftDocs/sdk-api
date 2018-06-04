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

# IWPCWebSettings interface


## -description


Accesses web restrictions settings for the user.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCWebSettings</b> interface inherits from <b>IWPCSettings</b>. <b>IWPCWebSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCWebSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf0c1a54-ac36-45f4-8005-1847dc00bf7f">GetSettings</a>
</td>
<td align="left" width="63%">
Retrieves the web restrictions settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e229b0e-59ae-4fcf-a398-32bc20611802">RequestURLOverride</a>
</td>
<td align="left" width="63%">
Requests that the Parental Controls web restrictions subsystem set the specified primary and sub URLs to the allowed state.

</td>
</tr>
</table> 

