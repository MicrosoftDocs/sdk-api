---
UID: NF:userenv.RefreshPolicyEx
title: RefreshPolicyEx function (userenv.h)
description: The RefreshPolicyEx function causes policy to be applied immediately on the computer. The extended function allows you to specify the type of policy refresh to apply.
helpviewer_keywords: ["RP_FORCE","RefreshPolicyEx","RefreshPolicyEx function [Group Policy]","_win32_refreshpolicyex","policy.refreshpolicyex","userenv/RefreshPolicyEx"]
old-location: policy\refreshpolicyex.htm
tech.root: Policy
ms.assetid: 905ab96b-a7f2-4bb4-a539-385f78284644
ms.date: 12/05/2018
ms.keywords: RP_FORCE, RefreshPolicyEx, RefreshPolicyEx function [Group Policy], _win32_refreshpolicyex, policy.refreshpolicyex, userenv/RefreshPolicyEx
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
 - RefreshPolicyEx
 - userenv/RefreshPolicyEx
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
 - RefreshPolicyEx
---

# RefreshPolicyEx function


## -description

The
    <b>RefreshPolicyEx</b> function causes policy to be applied immediately on the computer. The extended function allows you to specify the type of policy refresh to apply.

## -parameters

### -param bMachine [in]

Specifies whether to refresh the computer policy or user policy. If this value is <b>TRUE</b>, the system refreshes the computer policy. If this value is <b>FALSE</b>, the system refreshes the user policy.

### -param dwOptions [in]

Specifies the type of policy refresh to apply. This parameter can be the following value.



#### RP_FORCE

Reapply all policies even if no policy change was detected.

Note that if there are any client-side extensions that can be applied at boot or logon time, (for example, an application installation extension), the extensions are re-applied at the next boot or logon, even if no policy change is detected.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If you do not need to specify the <i>dwOptions</i> parameter, you can call the 
<a href="/windows/desktop/api/userenv/nf-userenv-refreshpolicy">RefreshPolicy</a> function instead.

By default, policy is reapplied every 90 minutes.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicyex">ProcessGroupPolicyEx</a>



<a href="/windows/desktop/api/userenv/nf-userenv-refreshpolicy">RefreshPolicy</a>