---
UID: NN:comsvcs.ISecurityCallersColl
title: ISecurityCallersColl (comsvcs.h)
description: Provides access to information about individual callers in a collection of callers.
helpviewer_keywords: ["ISecurityCallersColl","ISecurityCallersColl interface [COM+]","ISecurityCallersColl interface [COM+]","described","_cos_ISecurityCallersColl","comsvcs/ISecurityCallersColl","cos.isecuritycallerscoll"]
old-location: cos\isecuritycallerscoll.htm
tech.root: cos
ms.assetid: b9b16d2e-92fd-40d2-b33d-8a82a1291794
ms.date: 12/05/2018
ms.keywords: ISecurityCallersColl, ISecurityCallersColl interface [COM+], ISecurityCallersColl interface [COM+],described, _cos_ISecurityCallersColl, comsvcs/ISecurityCallersColl, cos.isecuritycallerscoll
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
 - ISecurityCallersColl
 - comsvcs/ISecurityCallersColl
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
 - ISecurityCallersColl
---

# ISecurityCallersColl interface


## -description

Provides access to information about individual callers in a collection of callers. The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller. Only callers who cross a boundary where security is checked are included in the chain of callers. (In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityidentitycoll">ISecurityIdentityColl</a>, an identity collection.

## -inheritance

The <b>ISecurityCallersColl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISecurityCallersColl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityidentitycoll">ISecurityIdentityColl</a>



<a href="/windows/desktop/cossdk/securitycallers">SecurityCallers</a>
