---
UID: NS:cfapi.CF_POPULATION_POLICY
title: CF_POPULATION_POLICY (cfapi.h)
description: Specifies the primary population policy and its modifier.
helpviewer_keywords: ["CF_POPULATION_POLICY","CF_POPULATION_POLICY structure","cfapi/CF_POPULATION_POLICY","cloudApi.cf_population_policy"]
old-location: cloudapi\cf_population_policy.htm
tech.root: cloudapi
ms.assetid: 043EBBF8-4077-429B-B959-55E0623520E2
ms.date: 04/04/2023
ms.keywords: CF_POPULATION_POLICY, CF_POPULATION_POLICY structure, cfapi/CF_POPULATION_POLICY, cloudApi.cf_population_policy
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
req.typenames: CF_POPULATION_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_POPULATION_POLICY
 - cfapi/CF_POPULATION_POLICY
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
 - CF_POPULATION_POLICY
---

# CF_POPULATION_POLICY structure

## -description

Specifies the primary population policy and its modifier. The population policy allows a sync provider to control how placeholder namespace (both directories and files) should be created by the platform.

## -struct-fields

### -field Primary

The primary population policy. See [CF_POPULATION_POLICY_PRIMARY](ne-cfapi-cf_population_policy_primary.md) for more information.

### -field Modifier

The population policy modifier. See [CF_POPULATION_POLICY_MODIFIER](ne-cfapi-cf_population_policy_modifier.md) for more information.

## -see-also

[CF_POPULATION_POLICY_PRIMARY](ne-cfapi-cf_population_policy_primary.md)

[CF_POPULATION_POLICY_MODIFIER](ne-cfapi-cf_population_policy_modifier.md)

[CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md)
