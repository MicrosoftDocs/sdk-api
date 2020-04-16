---
UID: NN:efswrtinterop.IProtectionPolicyManagerInterop
title: IProtectionPolicyManagerInterop (efswrtinterop.h)
description: Manages enterprise protection policy on protected content.helpviewer_keywords: ["EDP.iprotectionpolicymanagerinterop","IProtectionPolicyManagerInterop","IProtectionPolicyManagerInterop interface","IProtectionPolicyManagerInterop interface","described","efswrtinterop/IProtectionPolicyManagerInterop interface"]
old-location: edp\iprotectionpolicymanagerinterop.htm
tech.root: EDP
ms.assetid: AFA7F918-8730-40A2-871E-9356391B47F8
ms.date: 12/05/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop, IProtectionPolicyManagerInterop, IProtectionPolicyManagerInterop interface, IProtectionPolicyManagerInterop interface,described, efswrtinterop/IProtectionPolicyManagerInterop interface
f1_keywords:
- efswrtinterop/IProtectionPolicyManagerInterop
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
- IProtectionPolicyManagerInterop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProtectionPolicyManagerInterop interface


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Manages enterprise protection policy on protected content.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProtectionPolicyManagerInterop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProtectionPolicyManagerInterop interface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProtectionPolicyManagerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/efswrtinterop/nf-efswrtinterop-iprotectionpolicymanagerinterop-getforwindow">IProtectionPolicyManagerInterop::GetForWindow</a>
</td>
<td align="left" width="63%">
Returns the protection policy manager object associated with the current app window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/efswrtinterop/nf-efswrtinterop-iprotectionpolicymanagerinterop-requestaccessforwindowasync">IProtectionPolicyManagerInterop::RequestAccessForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise protected content for an identity.

</td>
</tr>
</table> 

