---
UID: NF:authz.AuthzFreeCentralAccessPolicyCache
title: AuthzFreeCentralAccessPolicyCache function (authz.h)
description: Decreases the CAP cache reference count by one so that the CAP cache can be deallocated.
helpviewer_keywords: ["AuthzFreeCentralAccessPolicyCache","AuthzFreeCentralAccessPolicyCache function [Security]","authz/AuthzFreeCentralAccessPolicyCache","security.authzfreecentralaccesspolicycache"]
old-location: security\authzfreecentralaccesspolicycache.htm
tech.root: security
ms.assetid: 0F972A95-3CD7-4C86-99DE-5B3D50CE9A34
ms.date: 12/05/2018
ms.keywords: AuthzFreeCentralAccessPolicyCache, AuthzFreeCentralAccessPolicyCache function [Security], authz/AuthzFreeCentralAccessPolicyCache, security.authzfreecentralaccesspolicycache
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuthzFreeCentralAccessPolicyCache
 - authz/AuthzFreeCentralAccessPolicyCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzFreeCentralAccessPolicyCache
---

# AuthzFreeCentralAccessPolicyCache function


## -description

The <b>AuthzFreeCentralAccessPolicyCache</b> function frees the cache maintained as a result of <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a> evaluating the Central Access Policies (CAP) that applies for the resource.



## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> and <a href="/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a> overviews.

## -see-also

<a href="/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>
