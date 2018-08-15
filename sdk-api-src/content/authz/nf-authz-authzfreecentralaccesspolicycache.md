---
UID: NF:authz.AuthzFreeCentralAccessPolicyCache
title: AuthzFreeCentralAccessPolicyCache function
author: windows-sdk-content
description: Decreases the CAP cache reference count by one so that the CAP cache can be deallocated.
old-location: security\authzfreecentralaccesspolicycache.htm
old-project: secauthz
ms.assetid: 0F972A95-3CD7-4C86-99DE-5B3D50CE9A34
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AuthzFreeCentralAccessPolicyCache, AuthzFreeCentralAccessPolicyCache function [Security], authz/AuthzFreeCentralAccessPolicyCache, security.authzfreecentralaccesspolicycache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: authz.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzFreeCentralAccessPolicyCache function


## -description


The <b>AuthzFreeCentralAccessPolicyCache</b> function frees the cache maintained as a result of <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a> evaluating the Central Access Policies (CAP) that applies for the resource.


## -parameters






## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information, see the <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a> and <a href="https://msdn.microsoft.com/5A06B8D8-F14B-4D9E-9ED6-4246A26BF945">Centralized Authorization Policy</a> overviews.




## -see-also




<a href="https://msdn.microsoft.com/5A06B8D8-F14B-4D9E-9ED6-4246A26BF945">Centralized Authorization Policy</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>
 

 

