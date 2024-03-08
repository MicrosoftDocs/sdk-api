---
UID: NF:cfapi.CfGetPlaceholderInfo
title: CfGetPlaceholderInfo function (cfapi.h)
description: Gets various characteristics of a placeholder file or folder.
helpviewer_keywords: ["CfGetPlaceholderInfo","CfGetPlaceholderInfo function","cfapi/CfGetPlaceholderInfo","cloudApi.cfgetplaceholderinfo"]
old-location: cloudapi\cfgetplaceholderinfo.htm
tech.root: cloudapi
ms.assetid: D82269CF-8056-46CF-9832-AAE8767A854B
ms.date: 03/30/2023
ms.keywords: CfGetPlaceholderInfo, CfGetPlaceholderInfo function, cfapi/CfGetPlaceholderInfo, cloudApi.cfgetplaceholderinfo
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
 - CfGetPlaceholderInfo
 - cfapi/CfGetPlaceholderInfo
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
 - CfGetPlaceholderInfo
---

# CfGetPlaceholderInfo function

## -description

Gets various characteristics of a placeholder file or folder. If the file is not a cloud files placeholder, the API will fail. On success, information is returned according to the specific *InfoClass* requested.

## -parameters

### -param FileHandle [in]

A handle to the placeholder whose information will be queried. Unlike most cloud files APIs that take a file handle, this one does not modify the file in any way. Therefore, the file handle only requires **READ_ATTRIBUTES** access.

### -param InfoClass [in]

Placeholder information. This can be set to either [CF_PLACEHOLDER_STANDARD_INFO](ns-cfapi-cf_placeholder_standard_info.md) or [CF_PLACEHOLDER_BASIC_INFO](ns-cfapi-cf_placeholder_basic_info.md).

### -param InfoBuffer [out]

A pointer to a buffer that will receive information about the placeholder.

### -param InfoBufferLength [in]

The length of the *InfoBuffer*, in bytes. If the buffer is not large enough to hold all the information requested, the API will return as much data as it can fit into the buffer, and the call will fail with **HRESULT_FROM_WIN32(ERROR_MORE_DATA)**.

### -param ReturnedLength [out, optional]

The number of bytes returned in the *InfoBuffer*.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

Placeholder information includes the following attributes:

| Attribute | Description |
|--------|--------|
| OnDiskDataSize | The total number of bytes on disk. |
| ValidatedDataSize | The total number of bytes that are in sync with the cloud. |
| ModifiedDataSize | The total number of bytes that have been overwritten/appended locally, i.e., not in sync with the cloud. |
| PropertiesSize | The total number of bytes on disk that is used by all the property blobs. |
| PinState | Refer to [CfSetPinState](nf-cfapi-cfsetpinstate.md) for more information. |
| InSyncState | Refer to [CfSetInSyncState](nf-cfapi-cfsetinsyncstate.md) for more information. |
| FileId | A 64-bit volume wide non-volatile number that uniquely identifies a file or directory. |
| SyncRootFileId | The file ID of the sync root directory under which the file whose placeholder information is to be queried resides. |
| FileIdentity | An opaque blob supplied by the sync provider to the platform when the placeholder was created. File identity is provided for all sync provider callbacks. |
| FileIdentityLength | The length of the file identity in bytes. |

## -see-also

[CfSetPinState](nf-cfapi-cfsetpinstate.md)

[CfSetInSyncState](nf-cfapi-cfsetinsyncstate.md)

[CF_PLACEHOLDER_STANDARD_INFO](ns-cfapi-cf_placeholder_standard_info.md)

[CF_PLACEHOLDER_BASIC_INFO](ns-cfapi-cf_placeholder_basic_info.md)
