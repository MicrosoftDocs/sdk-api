---
UID: NF:userenv.ProcessGroupPolicyCompletedEx
title: ProcessGroupPolicyCompletedEx function (userenv.h)
description: The ProcessGroupPolicyCompletedEx function notifies the system that the specified policy extension has finished applying policy. The function also reports the status of Resultant Set of Policy (RSoP) logging.
helpviewer_keywords: ["ProcessGroupPolicyCompletedEx","ProcessGroupPolicyCompletedEx function [Group Policy]","_win32_processgrouppolicycompletedex","policy.processgrouppolicycompletedex","userenv/ProcessGroupPolicyCompletedEx"]
old-location: policy\processgrouppolicycompletedex.htm
tech.root: Policy
ms.assetid: 0d899190-7345-4762-ab59-b89e2e87d10f
ms.date: 12/05/2018
ms.keywords: ProcessGroupPolicyCompletedEx, ProcessGroupPolicyCompletedEx function [Group Policy], _win32_processgrouppolicycompletedex, policy.processgrouppolicycompletedex, userenv/ProcessGroupPolicyCompletedEx
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
 - ProcessGroupPolicyCompletedEx
 - userenv/ProcessGroupPolicyCompletedEx
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
 - ProcessGroupPolicyCompletedEx
---

# ProcessGroupPolicyCompletedEx function


## -description

The 
    <b>ProcessGroupPolicyCompletedEx</b> function notifies the system that the specified policy extension has finished applying policy. The function also reports the status of Resultant Set of Policy (RSoP) logging.

## -parameters

### -param extensionId [in]

Specifies the unique <b>GUID</b> that identifies the policy extension.

### -param pAsyncHandle [in]

Asynchronous completion handle. This handle is passed to the 
<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicyex">ProcessGroupPolicyEx</a> callback function.

### -param dwStatus [in]

Specifies the completion status of asynchronous processing of policy.

### -param RsopStatus [in]

Specifies an <b>HRESULT</b> return code that indicates the status of RSoP logging.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a>



<a href="/windows/desktop/api/userenv/nf-userenv-processgrouppolicycompleted">ProcessGroupPolicyCompleted</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicyex">ProcessGroupPolicyEx</a>