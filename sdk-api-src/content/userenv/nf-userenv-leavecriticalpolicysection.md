---
UID: NF:userenv.LeaveCriticalPolicySection
title: LeaveCriticalPolicySection function (userenv.h)
description: The LeaveCriticalPolicySection function resumes the background application of policy. This function closes the handle to the policy section.
helpviewer_keywords: ["LeaveCriticalPolicySection","LeaveCriticalPolicySection function [Group Policy]","_win32_leavecriticalpolicysection","policy.leavecriticalpolicysection","userenv/LeaveCriticalPolicySection"]
old-location: policy\leavecriticalpolicysection.htm
tech.root: Policy
ms.assetid: 9e6a938f-c9cb-4baf-b7d0-4316e45f874c
ms.date: 12/05/2018
ms.keywords: LeaveCriticalPolicySection, LeaveCriticalPolicySection function [Group Policy], _win32_leavecriticalpolicysection, policy.leavecriticalpolicysection, userenv/LeaveCriticalPolicySection
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LeaveCriticalPolicySection
 - userenv/LeaveCriticalPolicySection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - LeaveCriticalPolicySection
---

# LeaveCriticalPolicySection function


## -description

The 
    <b>LeaveCriticalPolicySection</b> function resumes the background application of policy. This function closes the handle to the policy section.

## -parameters

### -param hSection [in]

Handle to a policy section, which is returned by the 
<a href="/windows/desktop/api/userenv/nf-userenv-entercriticalpolicysection">EnterCriticalPolicySection</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-entercriticalpolicysection">EnterCriticalPolicySection</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>