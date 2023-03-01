---
UID: NS:cfapi.CF_SYNC_POLICIES
title: CF_SYNC_POLICIES (cfapi.h)
description: Defines the sync policies used by a sync root.
helpviewer_keywords: ["CF_SYNC_POLICIES","CF_SYNC_POLICIES structure","cfapi/CF_SYNC_POLICIES","cloudApi.cf_sync_policies"]
old-location: cloudapi\cf_sync_policies.htm
tech.root: cloudapi
ms.assetid: 5BCD0958-1FED-4F97-A4B4-2EB354E85BF6
ms.date: 02/28/2023
ms.keywords: CF_SYNC_POLICIES, CF_SYNC_POLICIES structure, cfapi/CF_SYNC_POLICIES, cloudApi.cf_sync_policies
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
req.typenames: CF_SYNC_POLICIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_SYNC_POLICIES
 - cfapi/CF_SYNC_POLICIES
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
 - CF_SYNC_POLICIES
---

# CF_SYNC_POLICIES structure

## -description

Defines the sync policies used by a sync root.

## -struct-fields

### -field StructSize

The size of the `CF_SYNC_POLICIES` structure.

### -field Hydration

The hydration policy allows a sync provider to control how placeholder files should be hydrated by the platform. It consists of a primary policy and a set of policy modifiers.

The primary policy has four possible values:

| Policy | Description |
|--------|--------|
| ALWAYS_FULL | When `ALWAYS_FULL` is selected, the platform will fail, with HRESULT `ERROR_CLOUD_FILE_INVALID_REQUEST`, any placeholder operation that could result in a not fully hydrated placeholder, which includes [CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md), [CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85)), [CfUpdatePlaceholder](nf-cfapi-cfupdateplaceholder.md) with the _dehydrate_ option, and [CfConvertPlaceholder](nf-cfapi-cfconverttoplaceholder.md) with the _dehydrate_ option. |
| FULL | When `FULL` is selected, the platform will allow a placeholder to be dehydrated. When the platform detects access to a dehydrated placeholder, it will ensure that the full content of the placeholder is available locally before completing the user IO request, even if the request is only asking for 1 byte. |
| PROGRESSIVE | When `PROGRESSIVE` is selected, the platform will allow a placeholder to be dehydrated. When the platform detects access to a dehydrated placeholder, it will complete the user IO request as soon as it determines that sufficient data is received from the sync provider. However, the platform promises to continue requesting the remaining content in the placeholder from the sync provider in the background until either the full content of the placeholder is available locally or the last user handle on the placeholder is closed.<br/><br/> Note that sync providers who opt in for `PROGRESSIVE` may not assume that hydration callbacks arrive sequentially from offset 0. In other words, sync providers with `PROGRESSIVE` policy are expected to handle random seeks on the placeholder. |
| PARTIAL | The `PARTIAL` policy is very similar to `PROGRESSIVE`. The only difference between the two is the lack of continuous hydration in the background with the `PARTIAL` policy. |

Three policy modifiers are currently supported: `VALIDATION_REQUIRED`, `STREAMING_ALLOWED`, and `AUTO_DEHYDRATION_ALLOWED`. In general, modifiers can be mixed and matched with any primary policies and other policy modifiers as long as the combination is not self-conflicting.

| Policy modifier | Description |
|--------|--------|
| VALIDATION_REQUIRED | This policy modifier offers two guarantees to a sync provider. First, it guarantees that the data returned by the sync provider is always persisted to the disk prior to it being returned to the user application. Second, it allows the sync provider to retrieve the same data it has returned previously to the platform and validate its integrity. Only upon a successful confirmation of the integrity by the sync provider will the platform complete the user IO request. This modifier helps support end-to-end data integrity at the cost of extra disk IOs. |
| STREAMING_ALLOWED | This policy modifier grants the platform the permission to not store any data returned by a sync provider on local disks. This policy modifier is mutually exclusive with `VALIDATION_REQUIRED`. The API fails with `ERROR_INVALID_PARAMETER` when both flags are specified. |
| AUTO_DEHYDRATION_ALLOWED | This policy modifier grants the platform the permission to dehydrate in-sync cloud file placeholders without the help of sync providers. Without this flag, the platform is not allowed to call [CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85)) directly. Instead, the only supported way to dehydrate a cloud file placeholder is to clear the file’s pinned attribute and set the file’s unpinned attribute. Then the actual dehydration will be performed asynchronously by the sync engine after it receives the directory change notification on the two attributes. When this flag is specified, the platform will be allowed to invoke [CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85)) directly on any in-sync cloud file placeholder. It is recommended for sync providers to support auto dehydration. |
| ALLOW_FULL_RESTART_HYDRATION | This policy modifier grants the platform permission to fully hydrate a file synchronously when it intercepts an attempt by an AV Filter to scan the file. Sync providers that wish to use **RestartHydration** to change the `fileSize` from a **FetchData** callback must opt-in for the `ALLOW_FULL_RESTART_HYDRATION` policy to avoid possible deadlocks with anti-virus and anti-malware software trying to scan the file and the provider trying to change `fileSize` using **RestartHydration**.<br/><br/> **Note:** This modifier is supported only if the `PlatformVersion.IntegrationNumber` obtained from [CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md) is `0x500` or higher. |

### -field Population

The population policy allows a sync provider to control how placeholder namespace, both directories and files, should be created by the platform. There are currently three primary policies with no modifiers defined:

| Policy | Description |
|--------|--------|
| ALWAYS_FULL | When `ALWAYS_FULL` is selected, the platform assumes that the full name space is always available locally. It will never forward any directory enumeration request to the sync provider. |
| FULL | With the `FULL` population policy, when the platform detects access on a not fully populated directory, it will request the sync provider return all entries under the directory before completing the user request. |
| PARTIAL | With the `PARTIAL` population policy, when the platform detects access on a not fully populated directory, it will request only the entries required by the user application from the sync provider. |

### -field InSync

The `InSync` policy allows a sync provider to control when the platform should clear the in-sync state on a placeholder. In addition to always clearing in-sync on any data modification, the platform can currently clear in-sync on changes of any combinations of three file attributes (_ReadOnly_, _System_, and _Hidden_) and two file times (_CreateTime_ and _LastWriteTime_). These policies can be applied to files and directories separately.

### -field HardLink

By default, the platform does not allow hard links to be created on any placeholder. However, sync providers that are capable of handling hard links can instruct the platform to enable the support via the `ALLOWED` policy. With this policy, applications can create as many hard links as the file system supports so long as the links are under either the same sync root or no sync root. The platform will force a placeholder to be hydrated when the first out-of-sync-root link is introduced and revert a placeholder to normal file when its last in-sync-root link is removed. Hardlink creation that is not compatible with the policy will fail with HRESULT `ERROR_CLOUD_FILES_INCOMPATIBLE_HARDLINKS`. Placeholder operations that are not compatible with the policy will also fail with `ERROR_CLOUD_FILES_INCOMPATIBLE_HARDLINKS`.

### -field PlaceholderManagement

By default, only a sync provider can perform placeholder management operations in a sync root. Non sync provider processes can perform placeholder management operations only if the sync root is inactive (i.e., when no sync providers are connected to the sync root.) These policies, when enabled, allow non sync provider processes to perform respective placeholder management operations in an active sync root. `CF_PLACEHOLDER_MANAGEMENT_POLICY_DEFAULT` is the default policy, allowing only a connected sync provider to perform any placeholder management operations. The three policies below can be specified in any combination:

| Policy | Description |
|--------|--------|
| CF_PLACEHOLDER_MANAGEMENT_POLICY_CREATE_UNRESTRICTED | When this policy is specified during registration, any process can create a placeholder within an active sync root by calling [CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md). |
| CF_PLACEHOLDER_MANAGEMENT_POLICY_CONVERT_UNRESTRICTED | When this policy is specified during registration, any process can convert a file or a directory within an active sync root to a placeholder by calling [CfConvertToPlaceholder](nf-cfapi-cfconverttoplaceholder.md). |
| CF_PLACEHOLDER_MANAGEMENT_POLICY_UPDATE_UNRESTRICTED | When this policy is specified during registration, any process can update a placeholder within an active sync root via the API [CfUpdatePlaceholder](nf-cfapi-cfupdateplaceholder.md). |

> [!NOTE]
> These flags are supported only if the `PlatformVersion.IntegrationNumber` obtained from [CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md) is `0x310` or higher.

## -see-also

[CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md)

[CfConvertToPlaceholder](nf-cfapi-cfconverttoplaceholder.md)

[CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md)
