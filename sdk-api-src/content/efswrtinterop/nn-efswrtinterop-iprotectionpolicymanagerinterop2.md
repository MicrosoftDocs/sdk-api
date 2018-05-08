---
UID: NN:efswrtinterop.IProtectionPolicyManagerInterop2
title: IProtectionPolicyManagerInterop2
author: windows-driver-content
description: Manages enterprise protection policy on protected content.
old-location: edp\iprotectionpolicymanagerinterop2.htm
old-project: EDP
ms.assetid: B4B5BD4B-8F5F-4C1A-902E-5FB7FF75616B
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2, IProtectionPolicyManagerInterop2, IProtectionPolicyManagerInterop2 interface, IProtectionPolicyManagerInterop2 interface,described, efswrtinterop/IProtectionPolicyManagerInterop2 interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: efswrtinterop.h
req.include-header: 
req.target-type: Windows
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
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	efswrtinterop.h
api_name:
-	IProtectionPolicyManagerInterop2
product: Windows
targetos: Windows
req.lib: 
req.dll: Efswrt.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
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

