---
UID: NF:userenv.GetAppliedGPOListW
title: GetAppliedGPOListW function (userenv.h)
description: The GetAppliedGPOList function retrieves the list of GPOs applied for the specified user or computer. (Unicode)
helpviewer_keywords: ["GPO_LIST_FLAG_MACHINE", "GetAppliedGPOList", "GetAppliedGPOList function [Group Policy]", "GetAppliedGPOListW", "_win32_getappliedgpolist", "policy.getappliedgpolist", "userenv/GetAppliedGPOList", "userenv/GetAppliedGPOListW"]
old-location: policy\getappliedgpolist.htm
tech.root: Policy
ms.assetid: 11e80a4e-acc4-4229-aa34-8f7d083c1041
ms.date: 12/05/2018
ms.keywords: GPO_LIST_FLAG_MACHINE, GetAppliedGPOList, GetAppliedGPOList function [Group Policy], GetAppliedGPOListA, GetAppliedGPOListW, _win32_getappliedgpolist, policy.getappliedgpolist, userenv/GetAppliedGPOList, userenv/GetAppliedGPOListA, userenv/GetAppliedGPOListW
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetAppliedGPOListW (Unicode) and GetAppliedGPOListA (ANSI)
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
 - GetAppliedGPOListW
 - userenv/GetAppliedGPOListW
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
 - GetAppliedGPOList
 - GetAppliedGPOListA
 - GetAppliedGPOListW
---

# GetAppliedGPOListW function


## -description

The
    <b>GetAppliedGPOList</b> function retrieves the list of GPOs applied for the specified user or computer.

## -parameters

### -param dwFlags [in]

A value that specifies the policy type. This parameter can be the following value.



#### GPO_LIST_FLAG_MACHINE

Retrieves information  about the computer policy.

If this value is not specified, the function retrieves only user policy information.

### -param pMachineName [in]

A pointer to the name of the remote computer. The format of the name is "&#92;&#92;<i>computer_name</i>". If this parameter is <b>NULL</b>, the local computer name is used.

### -param pSidUser [in]

A value that specifies the SID of the user. If <i>pMachineName</i> is not <b>NULL</b> and <i>dwFlags</i> specifies user policy, then <i>pSidUser</i> cannot be <b>NULL</b>.

If <i>pMachineName</i> is <b>NULL</b> and <i>pSidUser</i> is <b>NULL</b>, the user is the currently logged-on user. If <i>pMachineName</i> is <b>NULL</b> and <i>pSidUser</i> is not <b>NULL</b>, the user is represented by <i>pSidUser</i> on the local computer. For more information, see 
<a href="/windows/desktop/SecAuthZ/security-identifiers">Security Identifiers</a>.

### -param pGuidExtension [in]

A value that specifies the <b>GUID</b> of the extension.

### -param ppGPOList [out]

A pointer that receives the list of GPO structures. For more information, see 
<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a>.


##### - dwFlags.GPO_LIST_FLAG_MACHINE

Retrieves information  about the computer policy.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns a system error code. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

To free the GPO list when you have finished processing it, call the 
<a href="/windows/desktop/api/userenv/nf-userenv-freegpolista">FreeGPOList</a> function.





> [!NOTE]
> The userenv.h header defines GetAppliedGPOList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-freegpolista">FreeGPOList</a>



<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getgpolista">GetGPOList</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>
