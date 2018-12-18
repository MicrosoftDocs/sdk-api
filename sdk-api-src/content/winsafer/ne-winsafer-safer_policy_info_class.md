---
UID: NE:winsafer._SAFER_POLICY_INFO_CLASS
title: SAFER_POLICY_INFO_CLASS
author: windows-sdk-content
description: Defines the ways in which a policy may be queried.
old-location: security\safer_policy_info_class.htm
tech.root: secmgmt
ms.assetid: e1438a9f-abca-463d-8a3a-3a820cba16e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SAFER_POLICY_INFO_CLASS, SAFER_POLICY_INFO_CLASS enumeration [Security], SaferPolicyDefaultLevel, SaferPolicyEnableTransparentEnforcement, SaferPolicyEvaluateUserScope, SaferPolicyLevelList, SaferPolicyScopeFlags, _mnp_safer_policy_info_class, security.safer_policy_info_class, winsafer/SAFER_POLICY_INFO_CLASS, winsafer/SaferPolicyDefaultLevel, winsafer/SaferPolicyEnableTransparentEnforcement, winsafer/SaferPolicyEvaluateUserScope, winsafer/SaferPolicyLevelList, winsafer/SaferPolicyScopeFlags
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_POLICY_INFO_CLASS
product: Windows
targetos: Windows
req.typenames: SAFER_POLICY_INFO_CLASS
req.redist: 
---

# SAFER_POLICY_INFO_CLASS enumeration


## -description


The <b>SAFER_POLICY_INFO_CLASS</b> enumeration type defines the ways in which a policy may be queried.


## -enum-fields




### -field SaferPolicyLevelList

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



The <b>SAFER_POLICY_INFO_CLASS</b> enumeration type is used by the <a href="https://msdn.microsoft.com/1c69d3c1-87e6-42cd-9acb-4c3d06801401">SaferGetPolicyInformation</a> function. 



