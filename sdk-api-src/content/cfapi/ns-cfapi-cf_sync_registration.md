---
UID: NS:cfapi.CF_SYNC_REGISTRATION
title: CF_SYNC_REGISTRATION (cfapi.h)
description: The details of the sync provider and sync root to be registered.
helpviewer_keywords: ["CF_SYNC_REGISTRATION","CF_SYNC_REGISTRATION structure","cfapi/CF_SYNC_REGISTRATION","cloudApi.cf_sync_registration"]
old-location: cloudapi\cf_sync_registration.htm
tech.root: cloudapi
ms.assetid: F4D535FA-A0F5-4B4E-8409-0DD13C78A94E
ms.date: 04/04/2023
ms.keywords: CF_SYNC_REGISTRATION, CF_SYNC_REGISTRATION structure, cfapi/CF_SYNC_REGISTRATION, cloudApi.cf_sync_registration
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
req.typenames: CF_SYNC_REGISTRATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_SYNC_REGISTRATION
 - cfapi/CF_SYNC_REGISTRATION
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
 - CF_SYNC_REGISTRATION
---

# CF_SYNC_REGISTRATION structure

## -description

The details of the sync provider and sync root to be registered.

## -struct-fields

### -field StructSize

The size of the **CF_SYNC_REGISTRATION** structure.

### -field ProviderName

The name of the sync provider. This is a user friendly string with a maximum length of 255 characters.

### -field ProviderVersion

The version of the sync provider. This is a user friendly string with a maximum length of 255 characters.

### -field SyncRootIdentity

The sync root identity used by the provider. This member is optional with a maximum size of 64 KB. The API fails with **ERROR_INVALID_PARAMETER** when the maximum length is exceeded. The platform will provide *SyncRootIdentity* back to the sync provider in any callbacks to the sync provider.

### -field SyncRootIdentityLength

The length of the *SyncRootIdentity*. This member is optional and is only used if a *SyncRootIdentity* is provided.

### -field FileIdentity

An optional file identity. This member has a maximum size of 4 KB. The API fails with **ERROR_INVALID_PARAMETER** when the maximum length is exceeded. The sync root *FileIdentity* blob will be provided only when the subject of the callback is the sync root itself.

### -field FileIdentityLength

The length of the *FileIdentity*. This member is optional and is only used if a *FileIdentity* is provided.

### -field ProviderId

This is a GUID that is meant to identify a specific sync provider. It is optional. If not provided, the platform generates a GUID using the MD5 hash of the *ProviderName* string. The information is used for telemetry only such that the platform can better correlate activities from the same sync provider more efficiently and more accurately even if the sync provider registers sync roots with different *ProviderName* strings. It is recommended that a sync provider always supply the same GUID for all versions of its sync product(s). On the other hand, sync providers are free to choose different *ProviderName* strings for the sake of the best user experience.

## -remarks

*SyncRootIdentity* and *SyncRootIdentityLength* are optional members. If not used, set *SyncRootIdentity* to `nullptr` and *SyncRootIdentityLength* to `0`. *FileIdentity* and *FileIdentityLength* are also optional and if not used should be set to `nullptr` and `0`, respectively.

## -see-also

[CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md)
