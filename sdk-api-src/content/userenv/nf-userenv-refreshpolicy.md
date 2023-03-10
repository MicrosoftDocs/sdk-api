---
UID: NF:userenv.RefreshPolicy
title: RefreshPolicy function (userenv.h)
description: The RefreshPolicy function causes policy to be applied immediately on the client computer.
helpviewer_keywords: ["RefreshPolicy","RefreshPolicy function [Group Policy]","_win32_refreshpolicy","policy.refreshpolicy","userenv/RefreshPolicy"]
old-location: policy\refreshpolicy.htm
tech.root: Policy
ms.assetid: e08cb006-d174-4506-87f0-580660bd4023
ms.date: 12/05/2018
ms.keywords: RefreshPolicy, RefreshPolicy function [Group Policy], _win32_refreshpolicy, policy.refreshpolicy, userenv/RefreshPolicy
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
 - RefreshPolicy
 - userenv/RefreshPolicy
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
 - RefreshPolicy
---

# RefreshPolicy function


## -description

The
    <b>RefreshPolicy</b> function causes policy to be applied immediately on the client computer. To apply policy and specify the type of refresh that should occur, you can call the extended function 
<a href="/windows/desktop/api/userenv/nf-userenv-refreshpolicyex">RefreshPolicyEx</a>.

## -parameters

### -param bMachine [in]

Specifies whether to refresh the computer policy or user policy. If this value is <b>TRUE</b>, the system refreshes the computer policy. If this value is <b>FALSE</b>, the system refreshes the user policy.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

By default, policy is reapplied every 90 minutes.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a>