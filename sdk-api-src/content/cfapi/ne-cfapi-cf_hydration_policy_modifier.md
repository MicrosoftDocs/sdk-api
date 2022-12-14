---
UID: NE:cfapi.CF_HYDRATION_POLICY_MODIFIER
title: CF_HYDRATION_POLICY_MODIFIER (cfapi.h)
description: Allows a sync provider to control how placeholder files should be hydrated by the platform. This is a modifier that can be used with the primary policy:\_CF_HYDRATION_POLICY_PRIMARY.
helpviewer_keywords: ["CF_HYDRATION_POLICY_MODIFIER","CF_HYDRATION_POLICY_MODIFIER enumeration","CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED","CF_HYDRATION_POLICY_MODIFIER_NONE","CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED","CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED","cfapi/CF_HYDRATION_POLICY_MODIFIER","cfapi/CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED","cfapi/CF_HYDRATION_POLICY_MODIFIER_NONE","cfapi/CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED","cfapi/CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED","cloudApi.cf_hydration_policy_modifier"]
old-location: cloudapi\cf_hydration_policy_modifier.htm
tech.root: cloudapi
ms.assetid: A98C635E-7E18-4E18-B19A-D3FD85A53CBB
ms.date: 12/05/2018
ms.keywords: CF_HYDRATION_POLICY_MODIFIER, CF_HYDRATION_POLICY_MODIFIER enumeration, CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED, CF_HYDRATION_POLICY_MODIFIER_NONE, CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED, CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED, cfapi/CF_HYDRATION_POLICY_MODIFIER, cfapi/CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED, cfapi/CF_HYDRATION_POLICY_MODIFIER_NONE, cfapi/CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED, cfapi/CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED, cloudApi.cf_hydration_policy_modifier
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
req.typenames: CF_HYDRATION_POLICY_MODIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_HYDRATION_POLICY_MODIFIER
 - cfapi/CF_HYDRATION_POLICY_MODIFIER
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
 - CF_HYDRATION_POLICY_MODIFIER
---

# CF_HYDRATION_POLICY_MODIFIER enumeration


## -description

Allows a sync provider to control how placeholder files should be hydrated by the platform. This is a modifier that can be used with the primary policy: <a href="/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary">CF_HYDRATION_POLICY_PRIMARY</a>.

## -enum-fields

### -field CF_HYDRATION_POLICY_MODIFIER_NONE:0x0000

No policy modifier.

### -field CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED:0x0001

This policy modifier offers two guarantees to a sync provider. First, it guarantees that the data returned by the sync provider is always persisted to the disk prior to it being returned to the user application. Second, it allows the sync provider to retrieve the same data it has returned previously to the platform and validate its integrity. Only upon a successful confirmation of the integrity by the sync provider will the platform complete the user I/O request. This modifier helps support end-to-end data integrity at the cost of extra disk I/Os.

### -field CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED:0x0002

This policy modifier grants the platform the permission to not store any data returned by a sync provider on local disks. This policy modifier is ineffective when being combined with <b>CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED</b>.

### -field CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED:0x0004

<b>Note</b>  This value is new for Windows 10, version 1803.

This policy modifier grants the platform the permission to dehydrate in-sync cloud file placeholders without the help of sync providers. Without this flag, the platform is not allowed to call <a href="/previous-versions/mt827480(v=vs.85)">CfDehydratePlaceholder</a> directly. Instead, the only supported way to dehydrate a cloud file placeholder is to clear the file’s pinned attribute and set the file’s unpinned attribute. At that point, the actual dehydration will be performed asynchronously by the sync engine after it receives the directory change notification on the two attributes. When this flag is specified, the platform will be allowed to invoke <b>CfDehydratePlaceholder</b> directly on any in-sync cloud file placeholder. It is recommended for sync providers to support auto-dehydration.

## -remarks

In general, modifiers can be mixed and matched with any primary policy (<a href="/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary">CF_HYDRATION_POLICY_PRIMARY</a>) and other policy modifiers so long as the combination is not self-conflicting.
