---
UID: NF:userenv.RsopSetPolicySettingStatus
title: RsopSetPolicySettingStatus function (userenv.h)
description: The RSoPSetPolicySettingStatus function creates an instance of RSOP_PolicySettingStatus and an instance of RSOP_PolicySettingLink. The function links (associates) RSOP_PolicySettingStatus to its RSOP_PolicySetting instance.
helpviewer_keywords: ["RSoPSetPolicySettingStatus","RSoPSetPolicySettingStatus function [Group Policy]","RsopSetPolicySettingStatus","_win32_rsopsetpolicysettingstatus","policy.rsopsetpolicysettingstatus","userenv/RSoPSetPolicySettingStatus"]
old-location: policy\rsopsetpolicysettingstatus.htm
tech.root: Policy
ms.assetid: 7ea2f217-4dd2-4c0f-af1b-d4bcb8707519
ms.date: 12/05/2018
ms.keywords: RSoPSetPolicySettingStatus, RSoPSetPolicySettingStatus function [Group Policy], RsopSetPolicySettingStatus, _win32_rsopsetpolicysettingstatus, policy.rsopsetpolicysettingstatus, userenv/RSoPSetPolicySettingStatus
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
 - RsopSetPolicySettingStatus
 - userenv/RsopSetPolicySettingStatus
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
 - RSoPSetPolicySettingStatus
---

# RsopSetPolicySettingStatus function


## -description

The 
    <b>RSoPSetPolicySettingStatus</b> function creates an instance of 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysettingstatus">RSOP_PolicySettingStatus</a> and an instance of 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysettinglink">RSOP_PolicySettingLink</a>. The function links (associates) 
<b>RSOP_PolicySettingStatus</b> to its 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysetting">RSOP_PolicySetting</a> instance.

## -parameters

### -param dwFlags [in]

This parameter is currently unused.

### -param pServices [in]

Specifies a WMI services pointer to the RSoP namespace to which the policy data is to be written. This parameter is required.

### -param pSettingInstance [in]

Pointer to an instance of 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysetting">RSOP_PolicySetting</a> containing the policy setting. This parameter is required and can point to the instance's children.

### -param nInfo [in]

Specifies the number of elements in the <i>pStatus</i> array.

### -param pStatus [in]

Pointer to an array of 
<a href="/windows/desktop/api/userenv/ns-userenv-policysettingstatusinfo">POLICYSETTINGSTATUSINFO</a> structures.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To unlink an 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysettingstatus">RSOP_PolicySettingStatus</a> instance from its 
<a href="/previous-versions/windows/desktop/Policy/rsop-policysetting">RSOP_PolicySetting</a> instance, you can call the 
<a href="/windows/desktop/api/userenv/nf-userenv-rsopresetpolicysettingstatus">RSoPResetPolicySettingStatus</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/userenv/nf-userenv-rsopresetpolicysettingstatus">RSoPResetPolicySettingStatus</a>