---
UID: NF:userenv.RsopResetPolicySettingStatus
title: RsopResetPolicySettingStatus function (userenv.h)
description: The RSoPResetPolicySettingStatus function unlinks the RSOP_PolicySettingStatus instance from its RSOP_PolicySetting instance.
helpviewer_keywords: ["RSoPResetPolicySettingStatus","RSoPResetPolicySettingStatus function [Group Policy]","RsopResetPolicySettingStatus","_win32_rsopresetpolicysettingstatus","policy.rsopresetpolicysettingstatus","userenv/RSoPResetPolicySettingStatus"]
old-location: policy\rsopresetpolicysettingstatus.htm
tech.root: Policy
ms.assetid: fd849efe-1ee7-4034-aea2-1a2bdb5e46bc
ms.date: 12/05/2018
ms.keywords: RSoPResetPolicySettingStatus, RSoPResetPolicySettingStatus function [Group Policy], RsopResetPolicySettingStatus, _win32_rsopresetpolicysettingstatus, policy.rsopresetpolicysettingstatus, userenv/RSoPResetPolicySettingStatus
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
 - RsopResetPolicySettingStatus
 - userenv/RsopResetPolicySettingStatus
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
 - RSoPResetPolicySettingStatus
---

# RsopResetPolicySettingStatus function


## -description

The 
    <b>RSoPResetPolicySettingStatus</b> function unlinks the 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysettingstatus">RSOP_PolicySettingStatus</a> instance from its 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysetting">RSOP_PolicySetting</a> instance. The function deletes the instances of 
<b>RSOP_PolicySettingStatus</b> and 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysettinglink">RSOP_PolicySettingLink</a>. Optionally, you can also specify that the function delete the instance of 
<b>RSOP_PolicySetting</b>.

## -parameters

### -param dwFlags [in]

This parameter is currently unused.

### -param pServices [in]

Specifies a WMI services pointer to the RSoP namespace to which the policy data is to be written. This parameter is required.

### -param pSettingInstance [in]

Pointer to an instance of 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysetting">RSOP_PolicySetting</a> containing the policy setting. This parameter is required and can also point to the instance's children.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To link (associate) the 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysettingstatus">RSOP_PolicySettingStatus</a> instance to its 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysetting">RSOP_PolicySetting</a> instance, you can call the 
<a href="/windows/desktop/api/userenv/nf-userenv-rsopsetpolicysettingstatus">RSoPSetPolicySettingStatus</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nf-userenv-rsopsetpolicysettingstatus">RSoPSetPolicySettingStatus</a>