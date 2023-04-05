---
UID: NF:cfapi.CfRegisterSyncRoot
title: CfRegisterSyncRoot function (cfapi.h)
description: Performs a one time sync root registration.
helpviewer_keywords: ["CfRegisterSyncRoot","CfRegisterSyncRoot function","cfapi/CfRegisterSyncRoot","cloudApi.cfregistersyncroot"]
old-location: cloudapi\cfregistersyncroot.htm
tech.root: cloudapi
ms.assetid: FAD56873-8812-42DC-9975-9507F73BD9E3
ms.date: 03/30/2023
ms.keywords: CfRegisterSyncRoot, CfRegisterSyncRoot function, cfapi/CfRegisterSyncRoot, cloudApi.cfregistersyncroot
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
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfRegisterSyncRoot
 - cfapi/CfRegisterSyncRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfRegisterSyncRoot
---

# CfRegisterSyncRoot function

## -description

Performs a one time sync root registration, allowing a sync provider to claim an entire directory tree structure, rooted at *SyncRootPath*, as their own to manage.

## -parameters

### -param SyncRootPath [in]

The path to the sync root to be registered.

### -param Registration [in]

Contains information about the sync provider and sync root to be registered.

**ProviderName** and **ProviderVersion** are end-user facing strings with a maximum length of 255 characters each.

Both **SyncRootIdentity** and **FileIdentity** are optional and when not provided their corresponding buffer lengths should be set to `0` as well. They are a way for a sync provider to persistently associate arbitrary data with a sync root.

The platform will provide **SyncRootIdentity** back to the sync provider in any callbacks to the sync provider. The sync root **FileIdentity** blob will be provided only when the subject of the callback is the sync root itself.

This facility is provided solely for the convenience of the sync provider, and both blobs have no special meaning outside of the sync provider.

The maximum-allowed length of **FileIdentity** is 4KB and the maximum-allowed length of **SyncRootIdentity** is 64KB. The API fails with **ERROR_INVALID_PARAMETER** when either maximum length is exceeded.

**ProviderId** is a GUID that is meant to identify a specific sync provider. It is optional. If not provided, the platform generates a GUID using the MD5 hash of the **ProviderName** string. The information is used for telemetry only such that the platform can better correlate activities from the same sync provider more efficiently and more accurately even if the sync provider registers sync roots with different **ProviderName** strings. It is recommended that a sync provider always supply the same GUID for all versions of its sync product(s). However, sync providers are free to choose different **ProviderName** strings for the sake of the best user experience.

### -param Policies [in]

The policies of the sync root to be registered.

### -param RegisterFlags [in]

Flags for registering previous and new sync roots.

| Flag | Description |
|--------|--------|
| **CF_REGISTER_FLAG_UPDATE** | A sync provider can pass **CF_REGISTER_FLAG_UPDATE** to re-register previously registered sync root identities and policies. |
| **CF_REGISTER_FLAG_DISABLE_ON_DEMAND_POPULATION_ON_ROOT** | The on-demand directory/folder population behavior is globally controlled by the population policy. This flag allows a sync provider to opt out of the on-demand population behavior just for the sync root itself while keeping on-demand population on for all other directories under the sync root. This is useful when the sync provider would like to pre-populate the immediate child files/directories of the sync root. |
| **CF_REGISTER_FLAG_MARK_IN_SYNC_ON_ROOT** | This flag allows a sync provider to mark the sync root to be registered in-sync simultaneously at the registration time. The alternative is to call [CfSetInSyncState](nf-cfapi-cfsetinsyncstate.md) on the sync root later. |

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

This can be used at a sync provider install time, first time set up for an individual user, or when a user configures another sync root (if this scenario is supported).

>[!NOTE]
>No two sync root trees are allowed to overlap. Because directory hard links are forbidden by the file system, the only way for two sync roots to overlap is if they have a direct ancestor/descendant relationship. The platform is responsible for persistently remembering all sync roots registered on a given volume, and failing any attempt to create overlapping sync roots.

A sync provider should have **WRITE_DATA** or **WRITE_DAC** access to the sync root to be registered or the registration will fail with **ERROR_CLOUD_FILE_ACCESS_DENIED**.

The sync provider should supply a registration record that contains various identities of the sync provider itself and the sync root to be registered, a set of policies that the platform uses to adjust its behavior on a per-sync-root basis, and a set of registration flags that allow finer control of the registration operation by the sync provider.

Unless explicitly called out as optional, all fields are mandatory and not providing them will result in the API call failing with an invalid parameter error.

All structures wherein future extensions are expected start with a **StructSize** field. The caller is responsible for the accurate accounting of the structure size.

The platform currently supports five types of *Policies*:

**Hydration Policy**

The hydration policy allows a sync provider to control how placeholder files should be hydrated by the platform. It consists of a primary policy and a set of policy modifiers.

The primary hydration policy has four different values:

| Policy | Description |
|--------|--------|
| **ALWAYS_FULL** | The platform will fail (with **ERROR_CLOUD_FILE_INVALID_REQUEST**) any placeholder operation that could result in a not fully hydrated placeholder, which includes [CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md), [CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85)), [CfUpdatePlaceholder](nf-cfapi-cfupdateplaceholder.md) with the dehydrate option, and [CfConvertToPlaceholder](nf-cfapi-cfconverttoplaceholder.md) with the dehydrate option. |
| **FULL** | The platform will allow a placeholder to be dehydrated. When the platform detects access to a dehydrated placeholder, it will ensure that the full content of the placeholder is available locally before completing the user IO request, even if the request is only asking for 1 byte. |
| **PROGRESSIVE** | The platform will allow a placeholder to be dehydrated. When the platform detects access to a dehydrated placeholder, it will complete the user IO request as soon as it determines that sufficient data is received from the sync provider. However, the platform promises to continue requesting the remaining content in the placeholder from the sync provider in the background until either the full content of the placeholder is available locally or the last user handle on the placeholder is closed. <br/><br/>**Note:** Sync providers that opt in for **PROGRESSIVE** may not assume that hydration callbacks arrive sequentially from offset `0`. In other words, sync providers with **PROGRESSIVE** policy are expected to handle random seeks on the placeholder. |
| **PARTIAL** | This policy is very similar to **PROGRESSIVE**, with the only difference being the lack of continuous hydration in the background. |

Three policy modifiers are currently supported. In general, modifiers can be mixed and matched with any primary policies and other policy modifiers so long as the combination is not self-conflicting.

| Modifier | Description |
|--------|--------|
| **VALIDATION_REQUIRED** | This policy modifier offers two guarantees to a sync provider. First, it guarantees that the data returned by the sync provider is always persisted to the disk prior to it being returned to the user application. Second, it allows the sync provider to retrieve the same data it has returned previously to the platform and validate its integrity. Only upon a successful confirmation of the integrity by the sync provider will the platform complete the user IO request. This modifier helps support end-to-end data integrity at the cost of extra disk IOs. |
| **STREAMING_ALLOWED** | This policy modifier grants the platform the permission to not store any data returned by a sync provider on local disks. This policy modifier is mutually exclusive with **VALIDATION_REQUIRED**. The API fails with **ERROR_INVALID_PARAMETER** when both flags are specified. |
| **AUTO_DEHYDRATION_ALLOWED** | This policy modifier grants the platform the permission to dehydrate in-sync cloud file placeholders without the help of sync providers. Without this flag, the platform is not allowed to call [CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85)) directly. Instead, the only supported way to dehydrate a cloud file placeholder is to clear the file’s pinned attribute and set the file’s unpinned attribute and then the actual dehydration will be performed asynchronously by the sync engine after it receives the directory change notification on the two attributes. When this flag is specified, the platform will be allowed to invoke **CfDehydratePlaceholder** directly on any in-sync cloud file placeholder. It is recommended for sync providers to support auto dehydration. |

**Population Policy**

The population policy allows a sync provider to control how placeholder namespace (both directories and files) should be created by the platform. There are currently three primary policies with no modifiers defined:

| Policy | Description |
|--------|--------|
| **ALWAYS_FULL** | The platform assumes that the full name space is always available locally. It will never forward any directory enumeration request to the sync provider. |
| **FULL** | When the platform detects access on a not fully populated directory, it will request the sync provider return all entries under the directory before completing the user request. |
| **PARTIAL** | When the platform detects access on a not fully populated directory, it will request only the entries required by the user application from the sync provider. |

**InSync Tracking Policy**

The **InSync** policy allows a sync provider to control when the platform should clear the in-sync state on a placeholder. In addition to always clearing in-sync on any data modification, the platform currently can clear in-sync on changes of any combinations of three file attributes (**ReadOnly**, **System**, and **Hidden**) and two file times (**CreateTime** and **LastWriteTime**). These policies can be applied to files and directories separately.

**Hardlink Policy**

By default, the platform does not allow hard links to be created on any placeholder. Sync providers that are capable of handling hard links however can instruct the platform to enable the support via the **ALLOWED** policy. With this policy, applications can create as many hard links as the file system supports so long as the links are under either the same sync root or no sync root. The platform will force a placeholder to be hydrated when the first out-of-sync-root link is introduced and revert a placeholder to normal file when its last in-sync-root link is removed. Hardlink creation that is not compatible with the policy will be failed with **STATUS_CLOUD_FILES_INCOMPATIBLE_HARDLINKS**. Placeholder operations that are not compatible with the policy will also be failed with **STATUS_CLOUD_FILES_INCOMPATIBLE_HARDLINKS**.

**Placeholder Management Policy**

By default, only a sync provider can perform placeholder management operations in a sync root. Non sync provider processes can perform placeholder management operations only if the sync root is inactive, i.e., when the sync root is not connected to by any sync provider. These policies, when enabled, allow non sync provider processes to perform respective placeholder management operations in an active sync root. **CF_PLACEHOLDER_MANAGEMENT_POLICY_DEFAULT** is the default policy allowing only a connected sync provider to perform any placeholder management operations. The following policies can be specified in any combination:

| Policy | Description |
|--------|--------|
| **CF_PLACEHOLDER_MANAGEMENT_POLICY_CREATE_UNRESTRICTED** | When this policy is specified during registration, any process can create a placeholder within an active sync root by calling [CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md). |
| **CF_PLACEHOLDER_MANAGEMENT_POLICY_CONVERT_UNRESTRICTED** | When this policy is specified during registration, any process can convert a file or a directory within an active sync root to a placeholder by calling [CfConvertToPlaceholder](nf-cfapi-cfconverttoplaceholder.md). |
| **CF_PLACEHOLDER_MANAGEMENT_POLICY_UPDATE_UNRESTRICTED** | When this policy is specified during registration, any process can update a placeholder within an active sync root by calling [CfUpdatePlaceholder](nf-cfapi-cfupdateplaceholder.md). |

>[!NOTE]
>These flags are supported only if **PlatformVersion.IntegrationNumber** obtained from [CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md) is `0x310` or higher.

## -see-also

[CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md)

[CfDehydratePlaceholder](/previous-versions/mt827480(v=vs.85))

[CfUpdatePlaceholder](nf-cfapi-cfupdateplaceholder.md)

[CfConvertToPlaceholder](nf-cfapi-cfconverttoplaceholder.md)

[CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md)

[CfSetInSyncState](nf-cfapi-cfsetinsyncstate.md)
