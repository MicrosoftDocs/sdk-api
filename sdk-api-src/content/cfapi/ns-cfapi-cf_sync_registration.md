---
UID: NS:cfapi.CF_SYNC_REGISTRATION
title: CF_SYNC_REGISTRATION (cfapi.h)
description: The details of the sync provider and sync root to be registered.
helpviewer_keywords: ["CF_SYNC_REGISTRATION","CF_SYNC_REGISTRATION structure","cfapi/CF_SYNC_REGISTRATION","cloudApi.cf_sync_registration"]
old-location: cloudapi\cf_sync_registration.htm
tech.root: cloudapi
ms.assetid: F4D535FA-A0F5-4B4E-8409-0DD13C78A94E
ms.date: 12/05/2018
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

The size of the structure.

### -field ProviderName

The name of the sync provider. This is a user friendly string with a maximum length of 255 characters.

### -field ProviderVersion

The version of the sync provider. This is a user friendly string with a maximum length of 255 characters.

### -field SyncRootIdentity

The sync root identity used by the provider. This member is optional with a maximum size of 64 KB.

### -field SyncRootIdentityLength

The length of the <b>SyncRootIdentity</b>. This member is optional and is only used if a <b>SyncRootIdentity</b> is provided.

### -field FileIdentity

An optional file identity. This member has a maximum size of 4 KB.

### -field FileIdentityLength

The length of the file identity.

### -field ProviderId

## -remarks

<b>SyncRootIdentity</b> and <b>SyncRootIdentityLength</b> are optional members. If not used, set <b>SyncRootIdentity</b> to <b>nullptr</b> and <b>SyncRootIdentityLength</b> to <b>0</b>. <b>FileIdentity</b> and <b>FileIdentityLength</b> are also optional and if not used should be set to <b>nullptr</b> and <b>0</b>, respectively.

