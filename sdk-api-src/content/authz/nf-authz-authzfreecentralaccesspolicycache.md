---
UID: NF:authz.AuthzFreeCentralAccessPolicyCache
title: AuthzFreeCentralAccessPolicyCache function (authz.h)
author: windows-sdk-content
description: Decreases the CAP cache reference count by one so that the CAP cache can be deallocated.
old-location: security\authzfreecentralaccesspolicycache.htm
tech.root: SecAuthZ
ms.assetid: 0F972A95-3CD7-4C86-99DE-5B3D50CE9A34
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AuthzFreeCentralAccessPolicyCache, AuthzFreeCentralAccessPolicyCache function [Security], authz/AuthzFreeCentralAccessPolicyCache, security.authzfreecentralaccesspolicycache
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzFreeCentralAccessPolicyCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuthzFreeCentralAccessPolicyCache function


## -description


The <b>AuthzFreeCentralAccessPolicyCache</b> function frees the cache maintained as a result of <a href="https://docs.microsoft.com/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a> evaluating the Central Access Policies (CAP) that applies for the resource.


## -parameters






## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



For more information, see the <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> and <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a> overviews.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>
 

 

