---
UID: NF:cfapi.CfOpenFileWithOplock
title: CfOpenFileWithOplock function (cfapi.h)
description: Opens an asynchronous opaque handle to a file or directory (for both normal and placeholder files) and sets up a proper oplock on it based on the open flags.
helpviewer_keywords: ["CfOpenFileWithOplock","CfOpenFileWithOplock function","cfapi/CfOpenFileWithOplock","cloudApi.cfopenfilewithoplock"]
old-location: cloudapi\cfopenfilewithoplock.htm
tech.root: cloudapi
ms.assetid: AFC48080-3B4A-4F6B-9122-25C2A025EA95
ms.date: 03/30/2023
ms.keywords: CfOpenFileWithOplock, CfOpenFileWithOplock function, cfapi/CfOpenFileWithOplock, cloudApi.cfopenfilewithoplock
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
 - CfOpenFileWithOplock
 - cfapi/CfOpenFileWithOplock
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
 - CfOpenFileWithOplock
---

# CfOpenFileWithOplock function

## -description

Opens an asynchronous opaque handle to a file or directory (for both normal and placeholder files) and sets up a proper oplock on it based on the open flags.

## -parameters

### -param FilePath [in]

Fully qualified path to the file or directory to be opened.

### -param Flags [in]

The flags to specify permissions on opening the file. *Flags* can be set to a combination of the following values:

- If **CF_OPEN_FILE_FLAG_EXCLUSIVE** is specified, the API returns a share-none handle and requests an **RH (OPLOCK_LEVEL_CACHE_READ|OPLOCK_LEVEL_CACHE_HANDLE)** oplock on the file; otherwise a share-all handle is opened and an **R (OPLOCK_LEVEL_CACHE_READ)** is requested.
- If **CF_OPEN_FILE_FLAG_WRITE_ACCESS** is specified, the API attempts to open the file or directory with **FILE_READ_DATA**/**FILE_LIST_DIRECTORY** and **FILE_WRITE_DATA**/**FILE_ADD_FILE** access; otherwise the API attempts to open the file or directory with **FILE_READ_DATA**/**FILE_LIST_DIRECTORY**.
- If **CF_OPEN_FILE_FLAG_DELETE_ACCESS** is specified, the API attempts to open the file or directory with **DELETE** access; otherwise it opens the file normally.

### -param ProtectedHandle [out]

An opaque handle to the file or directory that is just opened. Note that this is not a normal Win32 handle and hence cannot be used with non-CfApi Win32 APIs directly.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

When the oplock is broken, the API will handle the break notification automatically on behalf of the caller by draining all active requests and then closing the underlying Win32 handle.  

This aims to remove the complexity related to oplock usages. The caller must close the handle returned by **CfOpenFileWithOplock** with [CfCloseHandle](nf-cfapi-cfclosehandle.md).

## -see-also

[CfCloseHandle](nf-cfapi-cfclosehandle.md)
