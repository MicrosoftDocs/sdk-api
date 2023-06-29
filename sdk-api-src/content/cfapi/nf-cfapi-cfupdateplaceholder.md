---
UID: NF:cfapi.CfUpdatePlaceholder
title: CfUpdatePlaceholder function (cfapi.h)
description: Updates characteristics of the placeholder file or directory.
helpviewer_keywords: ["CfUpdatePlaceholder","CfUpdatePlaceholder function","cfapi/CfUpdatePlaceholder","cloudApi.cfupdateplaceholder"]
old-location: cloudapi\cfupdateplaceholder.htm
tech.root: cloudapi
ms.assetid: 13F2BF9A-505F-4CFB-B008-7DDE85A3C581
ms.date: 03/24/2023
ms.keywords: CfUpdatePlaceholder, CfUpdatePlaceholder function, cfapi/CfUpdatePlaceholder, cloudApi.cfupdateplaceholder
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
 - CfUpdatePlaceholder
 - cfapi/CfUpdatePlaceholder
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
 - CfUpdatePlaceholder
---

# CfUpdatePlaceholder function

## -description

This API changes characteristics of an existing placeholder. The most likely use of this API is when a file has been modified in the cloud, and the sync provider wishes to incorporate the effects of that modification into a placeholder. To support this scenario, the caller may pass in new file system metadata (timestamps, file size, etc.) to apply, and/or a new *FileIdentity* blob.

## -parameters

### -param FileHandle [in]

*FileHandle* is a handle to the file or directory whose metadata is to be updated. In the case of a file, the caller must acquire an exclusive handle to the file if it also intends to dehydrate the file at the same time or data corruption can occur. To minimize the impact on user applications, it is highly recommended that the caller obtain the exclusiveness using proper oplocks (via [CfOpenFileWithOplock](nf-cfapi-cfopenfilewithoplock.md)) as opposed to using a share-nothing handle.

### -param FsMetadata [in, optional]

*FsMetadata* contains file system metadata about the placeholder to be updated, including all timestamps, file attributes, and file size (optional for directories). This is an optional field. If not provided, all these fields remain intact after the call.

- A `0` value in a **timestamp** field (**CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime**) means no change to the current timestamp on the file.
- A `0` value in **FileAttributes** means no change to the current file attributes on the file.
- There is no special value in **FileSize**; a `0` value in **FileSize** truncates the file size to `0`.

### -param FileIdentity [in, optional]

*FileIdentity* is a user mode buffer that contains the opaque file or directory information supplied by the caller. The *FileIdentity* blob should not exceed 4KB in size. *FileIdentity* gets passed back to the sync provider in all callbacks. This is optional if an update is not needed or if the caller wants to remove the *FileIdentity* blob from the placeholder to be updated.

### -param FileIdentityLength [in]

Length, in bytes, of the *FileIdentity*.

### -param DehydrateRangeArray [in, optional]

This array specifies ranges of the existing placeholder that will no longer be considered valid after the update.

The simplest use of this parameter is to pass a single range, telling the platform that the entire byte range of data is now invalid. A more complex use of this parameter is to provide a series of discrete ranges to be considered invalid. This implies that the sync provider can distinguish changes on a sub-file level. All the offsets and lengths should be **PAGE_SIZE** Aligned. The platform will ensure that all the ranges specified get dehydrated as part of the update. If dehydration of any ranges fails the API will fail rather than result in torn file contents.

>[!NOTE]
>Passing a single range with Offset **0** and Length **CF_EOF** will invalidate the entire file - This has the same effect as passing the flag **CF_UPDATE_FLAG_DEHYDRATE** instead. Also, passing **CF_UPDATE_FLAG_DEHYDRATE** causes *DehydrateRangeArray* to be silently dropped

### -param DehydrateRangeCount [in]

The count of a series of discrete *DehydrateRangeArray* partitions of placeholder data.

### -param UpdateFlags [in]

Update flags for placeholders. UpdateFlags can be set to the following values:

| Flag | Description |
|--------|--------|
| **CF_UPDATE_FLAG_VERIFY_IN_SYNC** | The update will fail if the **IN_SYNC** attribute is not currently set on the placeholder. This is to prevent a race between syncing changes from the cloud down to a local placeholder and the placeholder’s data stream getting locally modified. |
| **CF_UPDATE_FLAG_MARK_IN_SYNC** | The platform marks the placeholder as in-sync upon a successful update placeholder operation. |
| **CF_UPDATE_FLAG_DEHYDRATE** | Applicable for files only. When specified, the platform dehydrates the file after updating the placeholder successfully. The caller must acquire an exclusive handle when specifying this flag or data corruptions can occur. Note that the platform does not validate the exclusiveness of the handle. |
| **CF_UPDATE_FLAG_ENABLE_ON_DEMAND_POPULATION** | Applicable for directories only. When specified, it marks the updated placeholder directory partially populated such that any future access to it will result in a **FETCH_PLACEHOLDERS** callback sent to the sync provider. |
| **CF_UPDATE_FLAG_DISABLE_ON_DEMAND_POPULATION** | Applicable for directories only. When specified, it marks the updated placeholder directory fully populated such that any future access to it will be handled by the platform without any callbacks to the sync provider. |
| **CF_UPDATE_FLAG_REMOVE_FILE_IDENTITY** | *FileIdentity* and *FileIdentityLength* are ignored and the platform will remove the existing file identity blob on the placeholder upon a successful update call. |
| **CF_UPDATE_FLAG_CLEAR_IN_SYNC** | The platform marks the placeholder as not in-sync upon a successful update placeholder operation. |
| **CF_UPDATE_FLAG_REMOVE_PROPERTY** | The platform removes all existing extrinsic properties on the placeholder. |
| **CF_UPDATE_FLAG_PASSTHROUGH_FS_METADATA** | The platform passes **CF_FS_METADATA** to the file system without any filtering; otherwise the platform skips setting any fields whose value is `0`. |
| **CF_UPDATE_FLAG_ALWAYS_FULL** | Effective on placeholder files only. When specified, the placeholder to be updated is marked always full. Once hydrated, any attempt to dehydrate such a placeholder file will fail with error code **ERROR_CLOUD_FILE_DEHYDRATION_DISALLOWED**. |
| **CF_UPDATE_FLAG_ALLOW_PARTIAL** | Effective on placeholder files only. When specified, the always full state on a placeholder file, if present, is cleared thus allowing it to be dehydrated again. It is invalid to specify this flag along with **CF_UPDATE_FLAG_ALWAYS_FULL** and error code **ERROR_CLOUD_FILE_INVALID_REQUEST** will be returned as a result. |

### -param UpdateUsn [in, out, optional]

On input, *UpdateUsn* instructs the platform to only perform the update if the file still has the same USN value as the one passed in. This serves a similar purpose to **CF_UPDATE_FLAG_VERIFY_IN_SYNC** but also encompasses local metadata changes. Passing a pointer to a USN value of `0` on input is the same as passing a `NULL` pointer.

On return, *UpdateUsn* receives the final USN value after update actions were performed.

### -param Overlapped [in, out, optional]

When specified and combined with an asynchronous *FileHandle*, *Overlapped* allows the platform to perform the **CfUpdatePlaceholder** call asynchronously. See the [Remarks](#-remarks) for more details.

If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

To update a placeholder:

- The placeholder to be updated must be contained in a registered sync root tree; it can be the sync root directory itself, or any descendant directory; otherwise, the call will be failed with **HRESULT(ERROR_CLOUD_FILE_NOT_UNDER_SYNC_ROOT)**.
- If dehydration is requested, the sync root must be registered with a valid hydration policy that is not **CF_HYDRATION_POLICY_ALWAYS_FULL**; otherwise the call will be failed with **HRESULT(ERROR_CLOUD_FILE_NOT_SUPPORTED)**.
- If dehydration is requested, the placeholder must not be pinned locally or the call will be failed with **HRESULT(ERROR_CLOUD_FILE_PINNED)**.
- If dehydration is requested, the placeholder must be in sync or the call will be failed with **HRESULT(ERROR_CLOUD_FILE_NOT_IN_SYNC)**.
- The caller must have **WRITE_DATA** or **WRITE_DAC** access to the placeholder to be updated. Otherwise the operation will be failed with **HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED)**.

If the API returns **HRESULT_FROM_WIN32(ERROR_IO_PENDING)** when using *Overlapped* asynchronously, the caller can then wait using [GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).

## -see-also

[CfOpenFileWithOplock](nf-cfapi-cfopenfilewithoplock.md)

[CF_UPDATE_FLAGS](ne-cfapi-cf_update_flags.md)
