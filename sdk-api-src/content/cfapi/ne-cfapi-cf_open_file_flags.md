---
UID: NE:cfapi.CF_OPEN_FILE_FLAGS
title: CF_OPEN_FILE_FLAGS
author: windows-sdk-content
description: Flags to request various permissions on opening a file.
old-location: cloudapi\cf_open_file_flags.htm
tech.root: cfApi
ms.assetid: 4A9D87AB-7B81-46DF-80C3-DB2F63C76964
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CF_OPEN_FILE_FLAGS, CF_OPEN_FILE_FLAGS enumeration, CF_OPEN_FILE_FLAG_DELETE_ACCESS, CF_OPEN_FILE_FLAG_EXCLUSIVE, CF_OPEN_FILE_FLAG_NONE, CF_OPEN_FILE_FLAG_WRITE_ACCESS, cfapi/CF_OPEN_FILE_FLAGS, cfapi/CF_OPEN_FILE_FLAG_DELETE_ACCESS, cfapi/CF_OPEN_FILE_FLAG_EXCLUSIVE, cfapi/CF_OPEN_FILE_FLAG_NONE, cfapi/CF_OPEN_FILE_FLAG_WRITE_ACCESS, cloudApi.cf_open_file_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_OPEN_FILE_FLAGS
product: Windows
targetos: Windows
req.typenames: CF_OPEN_FILE_FLAGS
req.redist: 
---

# CF_OPEN_FILE_FLAGS enumeration


## -description


Flags to request various permissions on opening a file.


## -enum-fields




### -field CF_OPEN_FILE_FLAG_NONE

No open file flags.


### -field CF_OPEN_FILE_FLAG_EXCLUSIVE

When specified, <a href="https://msdn.microsoft.com/AFC48080-3B4A-4F6B-9122-25C2A025EA95">CfOpenFileWithOplock</a> returns a share-none handle and requests an RH (OPLOCK_LEVEL_CACHE_READ|OPLOCK_LEVEL_CACHE_HANDLE) oplock on the file.


### -field CF_OPEN_FILE_FLAG_WRITE_ACCESS

When specified, <a href="https://msdn.microsoft.com/AFC48080-3B4A-4F6B-9122-25C2A025EA95">CfOpenFileWithOplock</a> attempts to open the file or directory with FILE_READ_DATA/FILE_LIST_DIRECTORY and FILE_WRITE_DATA/FILE_ADD_FILE access; otherwise it attempts to open the file or directory with FILE_READ_DATA/ FILE_LIST_DIRECTORY.


### -field CF_OPEN_FILE_FLAG_DELETE_ACCESS

When specified, <a href="https://msdn.microsoft.com/AFC48080-3B4A-4F6B-9122-25C2A025EA95">CfOpenFileWithOplock</a> attempts to open the file or directory with DELETE access; otherwise it opens the file normally.


### -field CF_OPEN_FILE_FLAG_FOREGROUND



