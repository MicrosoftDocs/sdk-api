---
UID: NS:cfapi.CF_PLACEHOLDER_CREATE_INFO
title: CF_PLACEHOLDER_CREATE_INFO (cfapi.h)
description: Contains placeholder information for creating new placeholder files or directories.
helpviewer_keywords: ["CF_PLACEHOLDER_CREATE_INFO","CF_PLACEHOLDER_CREATE_INFO structure","cfapi/CF_PLACEHOLDER_CREATE_INFO","cloudApi.cf_placeholder_create_info"]
old-location: cloudapi\cf_placeholder_create_info.htm
tech.root: cloudapi
ms.assetid: 2DC1FF5F-FBFD-45CA-8CD5-B2F586C22778
ms.date: 04/04/2023
ms.keywords: CF_PLACEHOLDER_CREATE_INFO, CF_PLACEHOLDER_CREATE_INFO structure, cfapi/CF_PLACEHOLDER_CREATE_INFO, cloudApi.cf_placeholder_create_info
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
req.typenames: CF_PLACEHOLDER_CREATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_PLACEHOLDER_CREATE_INFO
 - cfapi/CF_PLACEHOLDER_CREATE_INFO
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
 - CF_PLACEHOLDER_CREATE_INFO
---

# CF_PLACEHOLDER_CREATE_INFO structure

## -description

Contains placeholder information for creating new placeholder files or directories.

## -struct-fields

### -field RelativeFileName

The name of the child placeholder file or directory to be created. It should consist only of the file or directory name.

For example, if the sync root of the provider is C:\SyncRoot then to create a placeholder named placeholder.txt in a subdirectory of the sync root, call the [CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md) function with *BaseDirectoryPath* equal to `C:\SyncRoot\SubDirectory` and set the *RelativePathName* field of the **CF_PLACEHOLDER_CREATE_INFO** to `placeholder.txt`.

### -field FsMetadata

File system metadata to be created with the placeholder, including all timestamps, file attributes and file size (optional for directories).

### -field FileIdentity

A user mode buffer containing file information supplied by the sync provider. The *FileIdentity* blob should not exceed **CF_PLACEHOLDER_MAX_FILE_IDENTITY_LENGTH** (defined to 4KB) in size. *FileIdentity* gets passed back to the sync provider in all callbacks. This is required for files (not for directories).

### -field FileIdentityLength

Length, in bytes, of the *FileIdentity*.

### -field Flags

Flags for specifying placeholder creation behavior. See [CF_PLACEHOLDER_CREATE_FLAGS](ne-cfapi-cf_placeholder_create_flags.md) for more information.

### -field Result

The result of placeholder creation. On successful creation, the value is **STATUS_OK**.

### -field CreateUsn

The final USN value after create actions are performed.

## -see-also

[CF_PLACEHOLDER_CREATE_FLAGS](ne-cfapi-cf_placeholder_create_flags.md)

[CfCreatePlaceholders](nf-cfapi-cfcreateplaceholders.md)
