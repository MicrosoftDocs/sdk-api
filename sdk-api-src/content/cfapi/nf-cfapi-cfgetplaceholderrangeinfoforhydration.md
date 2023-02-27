---
UID: NF:cfapi.CfGetPlaceholderRangeInfoForHydration
tech.root: cloudapi
title: CfGetPlaceholderRangeInfoForHydration (cfapi.h)
ms.date: 02/27/2023
targetos: Windows
description: Gets range information about a placeholder file or folder using ConnectionKey, TransferKey and FileId as identifiers.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cfapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - cfapi.h
api_name:
 - CfGetPlaceholderRangeInfoForHydration
f1_keywords:
 - CfGetPlaceholderRangeInfoForHydration
 - cfapi/CfGetPlaceholderRangeInfoForHydration
dev_langs:
 - c++
helpviewer_keywords:
 - CfGetPlaceholderRangeInfoForHydration
---

## -description

Gets range information about a placeholder file or folder.

This range information is identical to what [CfGetPlaceholderRangeInfo](nf-cfapi-cfgetplaceholderrangeinfo.md) returns. However, it doesn’t take a **fileHandle** as a parameter. Instead, it uses `ConnectionKey`, `TransferKey`, and `FileId` to identify the file and the stream for which range information is being requested.

## -parameters

### -param ConnectionKey [in]

An opaque handle created by [CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md) for a sync root managed by the sync provider. It is returned also in `CF_CALLBACK_INFO` in the `CF_CALLBACK_TYPE_FETCH_DATA` callback and other callbacks.

### -param TransferKey [in]

The opaque handle to the placeholder file for which `CF_CALLBACK_TYPE_FETCH_DATA` callback has been invoked.

### -param FileId [in]

A unique ID of the placeholder file or directory to be serviced.

### -param InfoClass [in]

Types of the range of placeholder data.

### -param StartingOffset [in]

Offset of the starting point of the range of data.

### -param RangeLength [in]

Length of the range of data.

### -param InfoBuffer [out]

Pointer to a buffer that will receive the data. The buffer is an array of `CF_FILE_RANGE` structures, which are offset/length pairs, describing the requested ranges.

### -param InfoBufferSize [in]

The length of `InfoBuffer` in bytes.

### -param InfoBufferWritten [out, optional]

Receives the number of bytes returned in `InfoBuffer`.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an `HRESULT` error code.

## -remarks

The `InfoClass` value can be one of the following:

| Value | Description |
|--------|--------|
| CF_PLACEHOLDER_RANGE_INFO_ONDISK | On-disk data is data that is physical present in the file. This is a super set of other types of ranges. |
| CF_PLACEHOLDER_RANGE_INFO_VALIDATED | Validated data is a subset of the on-disk data that is currently in sync with the cloud. |
| CF_PLACEHOLDER_RANGEINFO_MODIFIED | Modified data is a subset of the on-disk data that is currently not in sync with the cloud (i.e., either modified or appended.) |

## -see-also

[CF_PLACEHOLDER_RANGE_INFO_CLASS](ne-cfapi-cf_placeholder_range_info_class.md)

[CfGetPlaceholderRangeInfo](nf-cfapi-cfgetplaceholderrangeinfo.md)

[CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md)
