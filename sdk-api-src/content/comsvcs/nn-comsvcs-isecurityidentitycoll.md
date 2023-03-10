---
UID: NN:comsvcs.ISecurityIdentityColl
title: ISecurityIdentityColl (comsvcs.h)
description: Provides access to a collection of security information representing a caller's identity. The items available in this collection are the SID, the account name, the authentication service, the authentication level, and the impersonation level.
helpviewer_keywords: ["ISecurityIdentityColl","ISecurityIdentityColl interface [COM+]","ISecurityIdentityColl interface [COM+]","described","_cos_ISecurityIdentityColl","comsvcs/ISecurityIdentityColl","cos.isecurityidentitycoll"]
old-location: cos\isecurityidentitycoll.htm
tech.root: cos
ms.assetid: 6844bfb2-028f-4155-85a6-b7023432f6cd
ms.date: 12/05/2018
ms.keywords: ISecurityIdentityColl, ISecurityIdentityColl interface [COM+], ISecurityIdentityColl interface [COM+],described, _cos_ISecurityIdentityColl, comsvcs/ISecurityIdentityColl, cos.isecurityidentitycoll
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ISecurityIdentityColl
 - comsvcs/ISecurityIdentityColl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityIdentityColl
---

# ISecurityIdentityColl interface


## -description

Provides access to a collection of security information representing a caller's identity. The items available in this collection are the SID, the account name, the authentication service, the authentication level, and the impersonation level.

This interface is used to find out about a particular caller in a chain of callers that is part of the security call context. For more information about how security call context information is accessed, see <a href="/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>. 

COM+ applications that do not use role-based security and base COM applications cannot call methods of <b>ISecurityIdentityColl</b> because they cannot obtain the necessary pointer to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>. For more information, see <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>.

## -inheritance

The <b>ISecurityIdentityColl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISecurityIdentityColl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallerscoll">ISecurityCallersColl</a>



<a href="/windows/desktop/cossdk/securityidentity">SecurityIdentity</a>
