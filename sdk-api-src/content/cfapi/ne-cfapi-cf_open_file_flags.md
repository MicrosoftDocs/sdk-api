---
UID: NE:cfapi.CF_OPEN_FILE_FLAGS
title: CF_OPEN_FILE_FLAGS (cfapi.h)
description: Flags to request various permissions on opening a file.
helpviewer_keywords: ["CF_OPEN_FILE_FLAGS","CF_OPEN_FILE_FLAGS enumeration","CF_OPEN_FILE_FLAG_DELETE_ACCESS","CF_OPEN_FILE_FLAG_EXCLUSIVE","CF_OPEN_FILE_FLAG_NONE","CF_OPEN_FILE_FLAG_WRITE_ACCESS","cfapi/CF_OPEN_FILE_FLAGS","cfapi/CF_OPEN_FILE_FLAG_DELETE_ACCESS","cfapi/CF_OPEN_FILE_FLAG_EXCLUSIVE","cfapi/CF_OPEN_FILE_FLAG_NONE","cfapi/CF_OPEN_FILE_FLAG_WRITE_ACCESS","cloudApi.cf_open_file_flags"]
old-location: cloudapi\cf_open_file_flags.htm
tech.root: cloudapi
ms.assetid: 4A9D87AB-7B81-46DF-80C3-DB2F63C76964
ms.date: 12/05/2018
ms.keywords: CF_OPEN_FILE_FLAGS, CF_OPEN_FILE_FLAGS enumeration, CF_OPEN_FILE_FLAG_DELETE_ACCESS, CF_OPEN_FILE_FLAG_EXCLUSIVE, CF_OPEN_FILE_FLAG_NONE, CF_OPEN_FILE_FLAG_WRITE_ACCESS, cfapi/CF_OPEN_FILE_FLAGS, cfapi/CF_OPEN_FILE_FLAG_DELETE_ACCESS, cfapi/CF_OPEN_FILE_FLAG_EXCLUSIVE, cfapi/CF_OPEN_FILE_FLAG_NONE, cfapi/CF_OPEN_FILE_FLAG_WRITE_ACCESS, cloudApi.cf_open_file_flags
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
req.typenames: CF_OPEN_FILE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_OPEN_FILE_FLAGS
 - cfapi/CF_OPEN_FILE_FLAGS
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
 - CF_OPEN_FILE_FLAGS
---

# CF_OPEN_FILE_FLAGS enumeration


## -description

Flags to request various permissions on opening a file.

## -enum-fields

### -field CF_OPEN_FILE_FLAG_NONE:0x00000000

No open file flags.

### -field CF_OPEN_FILE_FLAG_EXCLUSIVE:0x00000001

When specified, <a href="/windows/desktop/api/cfapi/nf-cfapi-cfopenfilewithoplock">CfOpenFileWithOplock</a> returns a share-none handle and requests an RH (OPLOCK_LEVEL_CACHE_READ\|OPLOCK_LEVEL_CACHE_HANDLE) oplock on the file.

### -field CF_OPEN_FILE_FLAG_WRITE_ACCESS:0x00000002

When specified, <a href="/windows/desktop/api/cfapi/nf-cfapi-cfopenfilewithoplock">CfOpenFileWithOplock</a> attempts to open the file or directory with FILE_READ_DATA/FILE_LIST_DIRECTORY and FILE_WRITE_DATA/FILE_ADD_FILE access; otherwise it attempts to open the file or directory with FILE_READ_DATA/ FILE_LIST_DIRECTORY.

### -field CF_OPEN_FILE_FLAG_DELETE_ACCESS:0x00000004

When specified, <a href="/windows/desktop/api/cfapi/nf-cfapi-cfopenfilewithoplock">CfOpenFileWithOplock</a> attempts to open the file or directory with DELETE access; otherwise it opens the file normally.

### -field CF_OPEN_FILE_FLAG_FOREGROUND:0x00000008
