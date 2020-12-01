---
UID: NN:tsgpolicyengine.ITSGPolicyEngine
title: ITSGPolicyEngine (tsgpolicyengine.h)
description: Exposes methods that authorize connections and resources.
helpviewer_keywords: ["ITSGPolicyEngine","ITSGPolicyEngine interface [Remote Desktop Services]","ITSGPolicyEngine interface [Remote Desktop Services]","described","termserv.itsgpolicyengine","tsgpolicyengine/ITSGPolicyEngine"]
old-location: termserv\itsgpolicyengine.htm
tech.root: TermServ
ms.assetid: 1972032f-48ac-4a15-98ce-9349fa158a07
ms.date: 12/05/2018
ms.keywords: ITSGPolicyEngine, ITSGPolicyEngine interface [Remote Desktop Services], ITSGPolicyEngine interface [Remote Desktop Services],described, termserv.itsgpolicyengine, tsgpolicyengine/ITSGPolicyEngine
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSGPolicyEngine
 - tsgpolicyengine/ITSGPolicyEngine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGPolicyEngine
---

# ITSGPolicyEngine interface


## -description

Exposes methods that authorize connections and resources. Implement this interface when you want to override the default authorization logic of Remote Desktop Gateway (RD Gateway).

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGPolicyEngine</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGPolicyEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSGPolicyEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-authorizeconnection">AuthorizeConnection</a>
</td>
<td align="left" width="63%">
Determines whether the specified connection is authorized to connect to  RD Gateway.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-authorizeresource">AuthorizeResource</a>
</td>
<td align="left" width="63%">
Determines which resources the specified connection is authorized to connect to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-isquarantineenabled">IsQuarantineEnabled</a>
</td>
<td align="left" width="63%">
Indicates whether the authorization plug-in requires a statement of health (SoH) from the user's computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-refresh">Refresh</a>
</td>
<td align="left" width="63%">
This method is reserved.

</td>
</tr>
</table>