---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SAFER_POLICY_INFO_CLASS enumeration


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



