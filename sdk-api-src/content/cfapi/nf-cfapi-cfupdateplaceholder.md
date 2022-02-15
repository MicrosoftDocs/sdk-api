---
UID: NF:cfapi.CfUpdatePlaceholder
title: CfUpdatePlaceholder function (cfapi.h)
description: Updates characteristics of the placeholder file or directory.
helpviewer_keywords: ["CfUpdatePlaceholder","CfUpdatePlaceholder function","cfapi/CfUpdatePlaceholder","cloudApi.cfupdateplaceholder"]
old-location: cloudapi\cfupdateplaceholder.htm
tech.root: cloudapi
ms.assetid: 13F2BF9A-505F-4CFB-B008-7DDE85A3C581
ms.date: 12/05/2018
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

Updates characteristics of the placeholder file or directory.

## -parameters

### -param FileHandle [in]

A handle to the file or directory whose metadata is to be updated.

### -param FsMetadata [in, optional]

File system metadata to be updated for the placeholder. Values of 0 for the metadata indicate there are no updates.

### -param FileIdentity [in, optional]

A user mode buffer that contains file or directory information supplied by the caller. Should not exceed 4KB in size.

### -param FileIdentityLength [in]

Length, in bytes, of the <i>FileIdentity</i>.

### -param DehydrateRangeArray [in, optional]

A range of an existing placeholder that will no longer be considered valid after the call to <b>CfUpdatePlaceholder</b>.

### -param DehydrateRangeCount [in]

The count of a series of discrete <i>DehydrateRangeArray</i> partitions of placeholder data.

### -param UpdateFlags [in]

Update flags for placeholders.

### -param UpdateUsn [in, out, optional]

On input, <i>UpdateUsn</i> instructs the platform to only perform the update if the file still has the same USN value as the one passed in.  This serves a similar purpose to <b>CF_UPDATE_FLAG_VERIFY_IN_SYNC</b> but also encompasses local metadata changes.  

On return, <i>UpdateUsn</i> receives the final USN value after update actions were performed.

### -param Overlapped [in, out, optional]

When specified and combined with an asynchronous <i>FileHandle</i>, <i>Overlapped</i> allows the platform to perform the <b>CfUpdatePlaceholder</b> call asynchronously. See the Remarks for more details.

If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To update a placeholder:

<ul>
<li>The placeholder to be updated must be contained in a registered sync root tree; it can be the sync root directory itself, or any descendant directory; otherwise, the call with be failed with HRESULT(ERROR_CLOUD_FILE_NOT_UNDER_SYNC_ROOT).
</li>
<li>If dehydration is requested, the sync root must be registered with a valid hydration policy that is not CF_HYDRATION_POLICY_ALWAYS_FULL; otherwise the call will be failed with HRESULT(ERROR_CLOUD_FILE_NOT_SUPPORTED).
</li>
<li>If dehydration is requested, the placeholder must not be pinned locally or the call with be failed with HRESULT(ERROR_CLOUD_FILE_PINNED).
</li>
<li>If dehydration is requested, the placeholder must be in sync or the call with be failed with HRESULT(ERROR_CLOUD_FILE_NOT_IN_SYNC).
</li>
<li>The caller must have WRITE_DATA or WRITE_DAC access to the placeholder to be updated. Otherwise the operation will be failed with HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED).
</li>
</ul>


If the API returns HRESULT_FROM_WIN32(ERROR_IO_PENDING) when using <i>Overlapped</i> asynchronously, the caller can then wait using <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>.