---
UID: NF:cfapi.CfOpenFileWithOplock
title: CfOpenFileWithOplock function (cfapi.h)
description: Opens an asynchronous opaque handle to a file or directory (for both normal and placeholder files) and sets up a proper oplock on it based on the open flags.
helpviewer_keywords: ["CfOpenFileWithOplock","CfOpenFileWithOplock function","cfapi/CfOpenFileWithOplock","cloudApi.cfopenfilewithoplock"]
old-location: cloudapi\cfopenfilewithoplock.htm
tech.root: cloudapi
ms.assetid: AFC48080-3B4A-4F6B-9122-25C2A025EA95
ms.date: 10/30/2023
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
  1. If **CF_OPEN_FILE_FLAG_EXCLUSIVE** is specified, the open is "share none" and it gets a (OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE) oplock.
     - A normal **CreateFile** call that opens for any of FILE_EXECUTE | FILE_READ_DATA | FILE_WRITE_DATA | FILE_APPEND_DATA | DELETE (or either/both of GENERIC_READ | GENERIC_WRITE) will break the oplock due to the sharing conflict. The oplock owner will get to finish and acknowledge.
  2. If **CF_OPEN_FILE_FLAG_EXCLUSIVE** is not specified, the open is "share all" and it gets a OPLOCK_LEVEL_CACHE_READ oplock.
     - A normal **CreateFile** call will not break the oplock.
     - If the normal **CreateFile** specifies a sharing mode that conflicts with the Cf handle's access (for instance, if the normal **CreateFile** does not specify FILE_SHARE_READ), the normal **CreateFile** will fail with ERROR_SHARING_VIOLATION.
     - The oplock doesn't break until the other caller issues a conflicting I/O, such as a write. When that happens the oplock break is advisory only.
- If **CF_OPEN_FILE_FLAG_WRITE_ACCESS** is specified, the API attempts to open the file or directory with **FILE_READ_DATA**/**FILE_LIST_DIRECTORY** and **FILE_WRITE_DATA**/**FILE_ADD_FILE** access; otherwise the API attempts to open the file or directory with **FILE_READ_DATA**/**FILE_LIST_DIRECTORY**.
- If **CF_OPEN_FILE_FLAG_DELETE_ACCESS** is specified, the API attempts to open the file or directory with **DELETE** access; otherwise it opens the file normally.
- If **CF_OPEN_FILE_FLAG_FOREGROUND** is specified, **CfOpenFileWithOplock** does not request an oplock. This should be used when the caller is acting as a foreground application. i.e., they don’t care whether the file handle created by this API causes sharing violations for other callers, and they don’t care about breaking any oplocks that may already be on the file. So, they open the handle without requesting an oplock.

    >[!NOTE]
    >The default *background* behavior requests an oplock when opening the file handle so that their call fails if there’s already an oplock, and they can be told to close their handle if they need to get out of the way to avoid causing a sharing violation later.
    >
    >Unless the caller specifies **CF_OPEN_FILE_FLAG_EXCLUSIVE** to **CfOpenFileWithOplock**, the oplock they get will be only **OPLOCK_LEVEL_CACHE_READ**, not **(OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE)**, so there won’t be the sharing violation protection a background app might normally want.

### -param ProtectedHandle [out]

An opaque handle to the file or directory that is just opened. Note that this is not a normal Win32 handle and hence cannot be used with non-CfApi Win32 APIs directly.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

When the oplock is broken, the API will handle the break notification automatically on behalf of the caller by draining all active requests and then closing the underlying Win32 handle.  

This aims to remove the complexity related to oplock usages. The caller must close the handle returned by **CfOpenFileWithOplock** with [CfCloseHandle](nf-cfapi-cfclosehandle.md).

A background application typically wants to operate transparently on files. In particular, they want to avoid causing sharing violations to other (foreground) openers. To do that, they take a (OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE) oplock, such as would be granted by using CF_OPEN_FILE_FLAG_EXCLUSIVE with **CfOpenFileWithOplock**. If another opener subsequently comes along whose requested share/access modes conflict with the background app's, then the background app's oplock breaks. This prompts the background app to close its file handle (for a Cf handle, that causes it to become invalid – the real underlying handle has been closed). Once the background app closes its handle, the other opener's open proceeds without encountering the sharing violation. This all works because of the OPLOCK_LEVEL_CACHE_HANDLE part of the oplock. Without CF_OPEN_FILE_FLAG_EXCLUSIVE, the oplock only has OPLOCK_LEVEL_CACHE_READ protection, so the sharing violation protection described doesn't happen.

## -see-also

[CfCloseHandle](nf-cfapi-cfclosehandle.md)

[CreateFile](../fileapi/nf-fileapi-createfilea.md)
