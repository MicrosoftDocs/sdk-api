---
UID: NS:cfapi.CF_HYDRATION_POLICY
title: CF_HYDRATION_POLICY (cfapi.h)
description: Specifies the primary hydration policy and its modifier.
helpviewer_keywords: ["CF_HYDRATION_POLICY","CF_HYDRATION_POLICY structure","cfapi/CF_HYDRATION_POLICY","cloudApi.cf_hydration_policy"]
old-location: cloudapi\cf_hydration_policy.htm
tech.root: cloudapi
ms.assetid: 1541E108-7AE4-4899-8940-94FD264C1B10
ms.date: 12/05/2018
ms.keywords: CF_HYDRATION_POLICY, CF_HYDRATION_POLICY structure, cfapi/CF_HYDRATION_POLICY, cloudApi.cf_hydration_policy
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_HYDRATION_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_HYDRATION_POLICY
 - cfapi/CF_HYDRATION_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_HYDRATION_POLICY
---

# CF_HYDRATION_POLICY structure

## -description

Specifies the [CF_HYDRATION_POLICY_PRIMARY](ne-cfapi-cf_hydration_policy_primary.md) and its [CF_HYDRATION_POLICY_MODIFIER](ne-cfapi-cf_hydration_policy_modifier.md).

## -struct-fields

### -field Primary

The primary hydration policy.

### -field Modifier

The hydration policy modifier.

## -remarks

The hydration policy allows a sync provider to control how placeholder files should be hydrated by the platform. It consists of a primary policy and a set of policy modifiers.

## -see-also

[CF_HYDRATION_POLICY_PRIMARY](ne-cfapi-cf_hydration_policy_primary.md)

[CF_HYDRATION_POLICY_MODIFIER](ne-cfapi-cf_hydration_policy_modifier.md)
