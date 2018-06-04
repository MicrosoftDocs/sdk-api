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

# IProtectionPolicyManagerInterop2 interface


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Manages enterprise protection policy on protected content.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProtectionPolicyManagerInterop2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProtectionPolicyManagerInterop2 interface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProtectionPolicyManagerInterop2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41F0047C-6442-4157-B710-E0DAF61DE44A">IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise-protected content for a specific target app.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9C631272-BF69-4CA5-9664-45C6831C252F">IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise protected content for an identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC0E0ED0-C8C3-4058-B20D-4F8BB3D83A87">IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise protected content for an identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91DEC69B-066E-427F-9C25-47B15EAD0D89">IProtectionPolicyManagerInterop2:RequestAccessForAppWithAuditingInfoForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise-protected content for a specific target app.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D78D0095-826A-4E6F-9420-873382A76B87">IProtectionPolicyManagerInterop2:RequestAccessForAppWithMessageForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise-protected content for a specific target app.

</td>
</tr>
</table> 

