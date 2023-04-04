---
UID: NS:cfapi.CF_FS_METADATA
title: CF_FS_METADATA (cfapi.h)
description: Placeholder file or directory metadata.
helpviewer_keywords: ["CF_FS_METADATA","CF_FS_METADATA structure","cfapi/CF_FS_METADATA","cloudApi.cf_fs_metadata"]
old-location: cloudapi\cf_fs_metadata.htm
tech.root: cloudapi
ms.assetid: A6D4473A-C93A-4B56-9EB0-9B44A56E5D28
ms.date: 04/04/2023
ms.keywords: CF_FS_METADATA, CF_FS_METADATA structure, cfapi/CF_FS_METADATA, cloudApi.cf_fs_metadata
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
req.typenames: CF_FS_METADATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_FS_METADATA
 - cfapi/CF_FS_METADATA
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
 - CF_FS_METADATA
---

# CF_FS_METADATA structure

## -description

Placeholder file or directory metadata, which can include all timestamps, file attributes and file size (optional for directories).

## -struct-fields

### -field BasicInfo

Basic file information in a [FILE_BASIC_INFO](/windows/win32/api/winbase/ns-winbase-file_basic_info) structure.

### -field FileSize

The size of the file, in bytes.

## -see-also

[FILE_BASIC_INFO](/windows/win32/api/winbase/ns-winbase-file_basic_info)
