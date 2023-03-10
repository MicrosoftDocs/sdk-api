---
UID: NN:aclui.ISecurityInformation3
title: ISecurityInformation3 (aclui.h)
description: Provides methods necessary for displaying an elevated access control editor when a user clicks the Edit button on an access control editor page that displays an image of a shield on that Edit button.
helpviewer_keywords: ["ISecurityInformation3","ISecurityInformation3 interface [Security]","ISecurityInformation3 interface [Security]","described","aclui/ISecurityInformation3","security.isecurityinformation3"]
old-location: security\isecurityinformation3.htm
tech.root: security
ms.assetid: e6cf92da-ebd2-4960-9df1-7124745df616
ms.date: 12/05/2018
ms.keywords: ISecurityInformation3, ISecurityInformation3 interface [Security], ISecurityInformation3 interface [Security],described, aclui/ISecurityInformation3, security.isecurityinformation3
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ISecurityInformation3
 - aclui/ISecurityInformation3
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
 - ISecurityInformation3
---

# ISecurityInformation3 interface


## -description

The <b>ISecurityInformation3</b> interface provides methods necessary for displaying an elevated access control editor when a user clicks the <b>Edit</b> button on an access control editor page that displays an image of a shield on that <b>Edit</b> button. The image of a shield is displayed on the <b>Edit</b> button when the access control editor is launched by a process with a token that lacks permission to save changes to the object being edited.

## -inheritance

The <b>ISecurityInformation3</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityInformation3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>
