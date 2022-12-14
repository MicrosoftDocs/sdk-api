---
UID: NN:aclui.ISecurityInformation2
title: ISecurityInformation2 (aclui.h)
description: Enables the access control editor to obtain information from the client that is not provided by the ISecurityInformation interface.
helpviewer_keywords: ["ISecurityInformation2","ISecurityInformation2 interface [Security]","ISecurityInformation2 interface [Security]","described","_win32_isecurityinformation2","aclui/ISecurityInformation2","security.isecurityinformation2"]
old-location: security\isecurityinformation2.htm
tech.root: security
ms.assetid: 5cb7a096-5088-424a-82d1-0351ce5bb413
ms.date: 12/05/2018
ms.keywords: ISecurityInformation2, ISecurityInformation2 interface [Security], ISecurityInformation2 interface [Security],described, _win32_isecurityinformation2, aclui/ISecurityInformation2, security.isecurityinformation2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityInformation2
 - aclui/ISecurityInformation2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation2
---

# ISecurityInformation2 interface


## -description

The <b>ISecurityInformation2</b> interface enables the access control editor to obtain information from the client that is not provided by the 
<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> interface. The client does not need to implement <b>ISecurityInformation2</b> unless the default behavior of the access control editor is unsuitable for the client.

## -inheritance

The <b>ISecurityInformation2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityInformation2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>
