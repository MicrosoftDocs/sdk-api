---
UID: NN:efswrtinterop.IProtectionPolicyManagerInterop2
title: IProtectionPolicyManagerInterop2 (efswrtinterop.h)
description: Manages enterprise protection policy on protected content.
old-location: edp\iprotectionpolicymanagerinterop2.htm
tech.root: EDP
ms.assetid: B4B5BD4B-8F5F-4C1A-902E-5FB7FF75616B
ms.date: 12/05/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2, IProtectionPolicyManagerInterop2, IProtectionPolicyManagerInterop2 interface, IProtectionPolicyManagerInterop2 interface,described, efswrtinterop/IProtectionPolicyManagerInterop2 interface
ms.topic: interface
f1_keywords:
- efswrtinterop/IProtectionPolicyManagerInterop2
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- efswrtinterop.h
api_name:
- IProtectionPolicyManagerInterop2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProtectionPolicyManagerInterop2 interface


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Manages enterprise protection policy on protected content.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProtectionPolicyManagerInterop2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProtectionPolicyManagerInterop2 interface</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/efswrtinterop/nf-efswrtinterop-iprotectionpolicymanagerinterop2-requestaccessforappwithwindowasync">IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise-protected content for a specific target app.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/efswrtinterop/nf-efswrtinterop-iprotectionpolicymanagerinterop2-requestaccesswithauditinginfoforwindowasync">IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise protected content for an identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/efswrtinterop/nf-efswrtinterop-iprotectionpolicymanagerinterop2-requestaccesswithmessageforwindowasync">IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise protected content for an identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/efswrtinterop/nf-efswrtinterop-iprotectionpolicymanagerinterop2-requestaccessforappwithauditinginfoforwindowasync">IProtectionPolicyManagerInterop2:RequestAccessForAppWithAuditingInfoForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise-protected content for a specific target app.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/efswrtinterop/nf-efswrtinterop-iprotectionpolicymanagerinterop2-requestaccessforappwithmessageforwindowasync">IProtectionPolicyManagerInterop2:RequestAccessForAppWithMessageForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise-protected content for a specific target app.

</td>
</tr>
</table> 

