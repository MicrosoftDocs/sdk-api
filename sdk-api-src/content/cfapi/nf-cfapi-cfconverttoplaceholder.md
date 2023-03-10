---
UID: NF:cfapi.CfConvertToPlaceholder
title: CfConvertToPlaceholder function (cfapi.h)
description: Converts a normal file/directory to a placeholder file/directory.
helpviewer_keywords: ["CfConvertToPlaceholder","CfConvertToPlaceholder function","cfapi/CfConvertToPlaceholder","cloudApi.cfconverttoplaceholder"]
old-location: cloudapi\cfconverttoplaceholder.htm
tech.root: cloudapi
ms.assetid: FDDE9CB0-E1A2-46D6-94E0-228495675271
ms.date: 12/05/2018
ms.keywords: CfConvertToPlaceholder, CfConvertToPlaceholder function, cfapi/CfConvertToPlaceholder, cloudApi.cfconverttoplaceholder
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
 - CfConvertToPlaceholder
 - cfapi/CfConvertToPlaceholder
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
 - CfConvertToPlaceholder
---

# CfConvertToPlaceholder function


## -description

Converts a normal file/directory to a placeholder file/directory.

## -parameters

### -param FileHandle [in]

Handle to the file or directory to be converted.

### -param FileIdentity [in, optional]

A user mode buffer that contains the opaque file or directory information supplied by the caller. Optional if the caller is not dehydrating the file at the same time, or if the caller is converting a directory. Cannot exceed 4KB in size.

### -param FileIdentityLength [in]

Length, in bytes, of the <i>FileIdentity</i>.

### -param ConvertFlags [in]

Placeholder conversion flags.

### -param ConvertUsn [out, optional]

The final USN value after convert actions are performed.

### -param Overlapped [in, out, optional]

When specified and combined with an asynchronous <i>FileHandle</i>, <i>Overlapped</i> allows the platform to perform the <b>CfConvertToPlaceholder</b> call asynchronously. See the Remarks for more details.

If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In the file case, the caller must acquire an exclusive handle to the file if it also intends to dehydrate the file at the same time or data corruption can occur. To minimize the impact on user applications it is highly recommended that the caller obtain the exclusiveness using proper oplocks (via <a href="/windows/desktop/api/cfapi/nf-cfapi-cfopenfilewithoplock">CfOpenFileWithOplock</a>) as opposed to using a share-nothing handle.


To convert a placeholder:

<ul>
<li>The file or directory to be converted must be contained in a registered sync root tree; it can be the sync root directory itself, or any descendant directory; otherwise, the call with be failed with HRESULT(ERROR_CLOUD_FILE_NOT_UNDER_SYNC_ROOT).
</li>
<li>If dehydration is requested, the sync root must be registered with a valid hydration policy that is not CF_HYDRATION_POLICY_ALWAYS_FULL; otherwise the call will be failed with HRESULT(ERROR_CLOUD_FILE_NOT_SUPPORTED).
</li>
<li>If dehydration is requested, the placeholder must not be pinned locally or the call with be failed with HRESULT(ERROR_CLOUD_FILE_PINNED).
</li>
<li>If dehydration is requested, the placeholder must be in sync or the call with be failed with HRESULT(ERROR_CLOUD_FILE_NOT_IN_SYNC).
</li>
<li>The caller must have WRITE_DATA or WRITE_DAC access to the file or directory to be converted. Otherwise the operation will be failed with HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED).
</li>
</ul>


If the API returns HRESULT_FROM_WIN32(ERROR_IO_PENDING) when using <i>Overlapped</i> asynchronously, the caller can then wait using <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>.