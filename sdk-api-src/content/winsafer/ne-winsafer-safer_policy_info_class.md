---
UID: NE:winsafer._SAFER_POLICY_INFO_CLASS
title: SAFER_POLICY_INFO_CLASS (winsafer.h)
description: Defines the ways in which a policy may be queried.
helpviewer_keywords: ["SAFER_POLICY_INFO_CLASS","SAFER_POLICY_INFO_CLASS enumeration [Security]","SaferPolicyDefaultLevel","SaferPolicyEnableTransparentEnforcement","SaferPolicyEvaluateUserScope","SaferPolicyLevelList","SaferPolicyScopeFlags","_mnp_safer_policy_info_class","security.safer_policy_info_class","winsafer/SAFER_POLICY_INFO_CLASS","winsafer/SaferPolicyDefaultLevel","winsafer/SaferPolicyEnableTransparentEnforcement","winsafer/SaferPolicyEvaluateUserScope","winsafer/SaferPolicyLevelList","winsafer/SaferPolicyScopeFlags"]
old-location: security\safer_policy_info_class.htm
tech.root: security
ms.assetid: e1438a9f-abca-463d-8a3a-3a820cba16e8
ms.date: 12/05/2018
ms.keywords: SAFER_POLICY_INFO_CLASS, SAFER_POLICY_INFO_CLASS enumeration [Security], SaferPolicyDefaultLevel, SaferPolicyEnableTransparentEnforcement, SaferPolicyEvaluateUserScope, SaferPolicyLevelList, SaferPolicyScopeFlags, _mnp_safer_policy_info_class, security.safer_policy_info_class, winsafer/SAFER_POLICY_INFO_CLASS, winsafer/SaferPolicyDefaultLevel, winsafer/SaferPolicyEnableTransparentEnforcement, winsafer/SaferPolicyEvaluateUserScope, winsafer/SaferPolicyLevelList, winsafer/SaferPolicyScopeFlags
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SAFER_POLICY_INFO_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_POLICY_INFO_CLASS
 - winsafer/_SAFER_POLICY_INFO_CLASS
 - SAFER_POLICY_INFO_CLASS
 - winsafer/SAFER_POLICY_INFO_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_POLICY_INFO_CLASS
---

# SAFER_POLICY_INFO_CLASS enumeration


## -description

The <b>SAFER_POLICY_INFO_CLASS</b> enumeration type defines the ways in which a policy may be queried.

## -enum-fields

### -field SaferPolicyLevelList:1

Queries for the list of all levels defined in a policy.

### -field SaferPolicyEnableTransparentEnforcement

Queries for the policy value to determine whether DLL checking is enabled.

### -field SaferPolicyDefaultLevel

Queries for the default policy level.

### -field SaferPolicyEvaluateUserScope

Queries to determine whether user scope rules should be consulted during policy evaluation.

### -field SaferPolicyScopeFlags

Queries to determine whether the policy is to skip members of the local administrators group.

### -field SaferPolicyDefaultLevelFlags

### -field SaferPolicyAuthenticodeEnabled

## -remarks

The <b>SAFER_POLICY_INFO_CLASS</b> enumeration type is used by the <a href="/windows/desktop/api/winsafer/nf-winsafer-safergetpolicyinformation">SaferGetPolicyInformation</a> function.
