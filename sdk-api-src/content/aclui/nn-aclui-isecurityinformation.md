---
UID: NN:aclui.ISecurityInformation
title: ISecurityInformation (aclui.h)
description: Enables the access control editor to communicate with the caller of the CreateSecurityPage and EditSecurity functions.
helpviewer_keywords: ["ISecurityInformation","ISecurityInformation interface [Security]","ISecurityInformation interface [Security]","described","_win32_isecurityinformation","aclui/ISecurityInformation","security.isecurityinformation"]
old-location: security\isecurityinformation.htm
tech.root: security
ms.assetid: 38d94f36-f149-4b62-a710-8f7359bfd8cd
ms.date: 12/05/2018
ms.keywords: ISecurityInformation, ISecurityInformation interface [Security], ISecurityInformation interface [Security],described, _win32_isecurityinformation, aclui/ISecurityInformation, security.isecurityinformation
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
 - ISecurityInformation
 - aclui/ISecurityInformation
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
 - ISecurityInformation
---

# ISecurityInformation interface


## -description

The <b>ISecurityInformation</b> interface enables the access control editor to communicate with the caller of the 
<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a> and 
<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a> functions. The editor calls the interface methods to retrieve information that is used to initialize its pages and to determine the editing options available to the user. The editor also calls the interface methods to pass the user's input back to the application.

The <b>LPSECURITYINFO</b> type is a pointer to an <b>ISecurityInformation</b> object.

## -inheritance

The <b>ISecurityInformation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityInformation</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>
