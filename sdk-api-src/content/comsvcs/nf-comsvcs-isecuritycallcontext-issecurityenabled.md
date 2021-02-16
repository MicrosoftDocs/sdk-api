---
UID: NF:comsvcs.ISecurityCallContext.IsSecurityEnabled
title: ISecurityCallContext::IsSecurityEnabled (comsvcs.h)
description: Determines whether security is enabled for the object.
helpviewer_keywords: ["ISecurityCallContext interface [COM+]","IsSecurityEnabled method","ISecurityCallContext.IsSecurityEnabled","ISecurityCallContext::IsSecurityEnabled","IsSecurityEnabled","IsSecurityEnabled method [COM+]","IsSecurityEnabled method [COM+]","ISecurityCallContext interface","_cos_ISecurityCallContext_IsSecurityEnabled","comsvcs/ISecurityCallContext::IsSecurityEnabled","cos.isecuritycallcontext_issecurityenabled"]
old-location: cos\isecuritycallcontext_issecurityenabled.htm
tech.root: cos
ms.assetid: b247d430-56b1-40be-a85a-5ed141d90c85
ms.date: 12/05/2018
ms.keywords: ISecurityCallContext interface [COM+],IsSecurityEnabled method, ISecurityCallContext.IsSecurityEnabled, ISecurityCallContext::IsSecurityEnabled, IsSecurityEnabled, IsSecurityEnabled method [COM+], IsSecurityEnabled method [COM+],ISecurityCallContext interface, _cos_ISecurityCallContext_IsSecurityEnabled, comsvcs/ISecurityCallContext::IsSecurityEnabled, cos.isecuritycallcontext_issecurityenabled
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
 - ISecurityCallContext::IsSecurityEnabled
 - comsvcs/ISecurityCallContext::IsSecurityEnabled
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
 - ISecurityCallContext.IsSecurityEnabled
---

# ISecurityCallContext::IsSecurityEnabled


## -description

Determines whether security is enabled for the object.

## -parameters

### -param pfIsEnabled [out]

<b>TRUE</b> if the application uses role-based security and role checking is currently enabled for the object; otherwise, <b>FALSE</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

COM+ applications can use one of two types of security: role-based security or process access permissions. If role-based security is being used by the application but is currently disabled, either at the application or component level, <i>pfIsEnabled</i> is  <b>FALSE</b>. Similarly, if the COM+ application uses process access permissions instead of role-based security, <i>pfIsEnabled</i> is <b>FALSE</b>.

You can use this method to find out whether role-based security is enabled before you check role membership using <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole">IsCallerInRole</a>. The reason for doing this is that <b>IsCallerInRole</b> is <b>TRUE</b> when role-based security is not enabled.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>



<a href="/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>



<a href="/windows/desktop/cossdk/role-based-security-administration">Role-Based Security</a>