---
UID: NE:cfapi.CF_HYDRATION_POLICY_MODIFIER
title: CF_HYDRATION_POLICY_MODIFIER (cfapi.h)
description: Allows a sync provider to control how placeholder files should be hydrated by the platform. This is a modifier that can be used with the primary policy:\_CF_HYDRATION_POLICY_PRIMARY.
helpviewer_keywords: ["CF_HYDRATION_POLICY_MODIFIER","CF_HYDRATION_POLICY_MODIFIER enumeration","CF_HYDRATION_POLICY_MODIFIER_ALLOW_FULL_RESTART_HYDRATION","CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED","CF_HYDRATION_POLICY_MODIFIER_NONE","CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED","CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED","cfapi/CF_HYDRATION_POLICY_MODIFIER","cfapi/CF_HYDRATION_POLICY_MODIFIER_ALLOW_FULL_RESTART_HYDRATION","cfapi/CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED","cfapi/CF_HYDRATION_POLICY_MODIFIER_NONE","cfapi/CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED","cfapi/CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED","cloudApi.cf_hydration_policy_modifier"]
old-location: cloudapi\cf_hydration_policy_modifier.htm
tech.root: cloudapi
ms.assetid: A98C635E-7E18-4E18-B19A-D3FD85A53CBB
ms.date: 02/28/2023
ms.keywords: CF_HYDRATION_POLICY_MODIFIER, CF_HYDRATION_POLICY_MODIFIER enumeration, CF_HYDRATION_POLICY_MODIFIER_ALLOW_FULL_RESTART_HYDRATION, CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED, CF_HYDRATION_POLICY_MODIFIER_NONE, CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED, CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED, cfapi/CF_HYDRATION_POLICY_MODIFIER, cfapi/CF_HYDRATION_POLICY_MODIFIER_ALLOW_FULL_RESTART_HYDRATION, cfapi/CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED, cfapi/CF_HYDRATION_POLICY_MODIFIER_NONE, cfapi/CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED, cfapi/CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED, cloudApi.cf_hydration_policy_modifier
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

Allows a sync provider to control how placeholder files should be hydrated by the platform. This is a modifier that can be used with the primary policy: [CF_HYDRATION_POLICY_PRIMARY](/windows/win32/api/cfapi/ne-cfapi-cf_hydration_policy_primary).

## -enum-fields

### -field CF_HYDRATION_POLICY_MODIFIER_NONE

`0x0000`

No policy modifier.

### -field CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED

`0x0001`

This policy modifier offers two guarantees to a sync provider. First, it guarantees that the data returned by the sync provider is always persisted to the disk prior to it being returned to the user application. Second, it allows the sync provider to retrieve the same data it has returned previously to the platform and validate its integrity. Only upon a successful confirmation of the integrity by the sync provider will the platform complete the user I/O request. This modifier helps support end-to-end data integrity at the cost of extra disk I/Os.

### -field CF_HYDRATION_POLICY_MODIFIER_STREAMING_ALLOWED

`0x0002`

This policy modifier grants the platform the permission to not store any data returned by a sync provider on local disks. This policy modifier is ineffective when being combined with **CF_HYDRATION_POLICY_MODIFIER_VALIDATION_REQUIRED**.

### -field CF_HYDRATION_POLICY_MODIFIER_AUTO_DEHYDRATION_ALLOWED

`0x0004`

This policy modifier grants the platform the permission to dehydrate in-sync cloud file placeholders without the help of sync providers. Without this flag, the platform is not allowed to call [CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85)) directly. Instead, the only supported way to dehydrate a cloud file placeholder is to clear the file’s pinned attribute and set the file’s unpinned attribute. At that point, the actual dehydration will be performed asynchronously by the sync engine after it receives the directory change notification on the two attributes. When this flag is specified, the platform will be allowed to invoke **CfDehydratePlaceholder** directly on any in-sync cloud file placeholder. It is recommended for sync providers to support auto-dehydration.

> [!NOTE]
> This value is available in Windows 10, version 1803 and later.

### -field CF_HYDRATION_POLICY_MODIFIER_ALLOW_FULL_RESTART_HYDRATION

`0x0008`

This policy modifier grants the platform permission to fully hydrate a file synchronously when it intercepts an attempt by an AV Filter to scan the file. Sync providers that wish to use **RestartHydration** to change the `fileSize` from a **FetchData** callback must opt-in for the `ALLOW_FULL_RESTART_HYDRATION` policy to avoid possible deadlocks with anti-virus and anti-malware software trying to scan the file and the provider trying to change `fileSize` using **RestartHydration**.

> [!NOTE]
> This enum update is supported only if the `PlatformVersion.IntegrationNumber` obtained from [CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md) is `0x500` or higher.

## -remarks

In general, modifiers can be mixed and matched with any primary policy ([CF_HYDRATION_POLICY_PRIMARY](/windows/win32/api/cfapi/ne-cfapi-cf_hydration_policy_primary)) and other policy modifiers so long as the combination is not self-conflicting.

The `CF_HYDRATION_POLICY_MODIFIER_ALLOW_FULL_RESTART_HYDRATION` flag is added to avoid the Restart Hydration feature from encountering deadlocks caused by Anti-Virus and Malware detectors (AV). All Sync Providers that intend to update the file size of a dehydrated file during the course of a hydration request should opt-in for this feature or restart hydration may run into deadlock when an AV attempts to scan a file being opened by creating a memory mapped section of the file and that leads to hydration. Note that providers that maintain snapshots or versions of a file and satisfy a user's request by supplying the requested version of the file even though the file has been updated in the backend/server need not opt in for this policy. Similarly, providers that fail the hydration request in case the file has changed in the backend may not opt-in for this policy.

## -see-also

[CF_HYDRATION_POLICY_PRIMARY](/windows/win32/api/cfapi/ne-cfapi-cf_hydration_policy_primary)

[CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85))

[CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md)
