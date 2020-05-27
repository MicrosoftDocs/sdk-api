---
UID: NN:aclui.ISecurityInformation2
title: ISecurityInformation2 (aclui.h)
description: Enables the access control editor to obtain information from the client that is not provided by the ISecurityInformation interface.
helpviewer_keywords: ["ISecurityInformation2","ISecurityInformation2 interface [Security]","ISecurityInformation2 interface [Security]","described","_win32_isecurityinformation2","aclui/ISecurityInformation2","security.isecurityinformation2"]
old-location: security\isecurityinformation2.htm
tech.root: SecAuthZ
ms.assetid: 5cb7a096-5088-424a-82d1-0351ce5bb413
ms.date: 12/05/2018
ms.keywords: ISecurityInformation2, ISecurityInformation2 interface [Security], ISecurityInformation2 interface [Security],described, _win32_isecurityinformation2, aclui/ISecurityInformation2, security.isecurityinformation2
f1_keywords:
- aclui/ISecurityInformation2
dev_langs:
- c++
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Aclui.h
api_name:
- ISecurityInformation2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityInformation2 interface


## -description


The <b>ISecurityInformation2</b> interface enables the access control editor to obtain information from the client that is not provided by the 
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> interface. The client does not need to implement <b>ISecurityInformation2</b> unless the default behavior of the access control editor is unsuitable for the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityInformation2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityInformation2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityInformation2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation2-isdaclcanonical">IsDaclCanonical</a>
</td>
<td align="left" width="63%">
Checks the specified DACL for canonical ordering of the ACEs contained within it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation2-lookupsids">LookupSids</a>
</td>
<td align="left" width="63%">
Retrieves the common names corresponding to the specified SIDs.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>
 

 

