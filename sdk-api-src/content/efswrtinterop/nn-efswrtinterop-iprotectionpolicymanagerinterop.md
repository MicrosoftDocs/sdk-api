---
UID: NN:efswrtinterop.IProtectionPolicyManagerInterop
title: IProtectionPolicyManagerInterop
author: windows-sdk-content
description: Manages enterprise protection policy on protected content.
old-location: edp\iprotectionpolicymanagerinterop.htm
tech.root: EDP
ms.assetid: AFA7F918-8730-40A2-871E-9356391B47F8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop, IProtectionPolicyManagerInterop, IProtectionPolicyManagerInterop interface, IProtectionPolicyManagerInterop interface,described, efswrtinterop/IProtectionPolicyManagerInterop interface
ms.prod: windows
ms.technology: windows-sdk
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProtectionPolicyManagerInterop interface


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Manages enterprise protection policy on protected content.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProtectionPolicyManagerInterop</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProtectionPolicyManagerInterop interface</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/638316E0-8D5C-4966-A44F-8F31ECBE83EB">IProtectionPolicyManagerInterop::GetForWindow</a>
</td>
<td align="left" width="63%">
Returns the protection policy manager object associated with the current app window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F32A24C6-0913-4EB9-8462-6AA734429D7E">IProtectionPolicyManagerInterop::RequestAccessForWindowAsync</a>
</td>
<td align="left" width="63%">
Request access to enterprise protected content for an identity.

</td>
</tr>
</table> 

