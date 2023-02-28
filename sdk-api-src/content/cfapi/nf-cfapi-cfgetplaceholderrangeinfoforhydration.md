---
UID: NF:cfapi.CfGetPlaceholderRangeInfoForHydration
tech.root: cloudapi
title: CfGetPlaceholderRangeInfoForHydration (cfapi.h)
ms.date: 02/28/2023
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

> [!NOTE]
> This API is available only if the `PlatformVersion.IntegrationNumber` obtained from [CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md) is `0x600` or higher.

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

While an API to query hydrated file ranges of a placeholder already exists, a new API was needed for improving reliability of the platform.

The existing API, [CfGetPlaceholderRangeInfo](nf-cfapi-cfgetplaceholderrangeinfo.md), requires an opened handle to a file and then triggers a `FSCTL_HSM_CONTROL` using that handle. Providers/Sync Engines normally use this API to assess which portions of the file aren’t hydrated from the context of a `CF_CALLBACK_TYPE_FETCH_DATA` callback invoked by the filter to hydrate the file to satisfy an IO.

A mini filter in the IO stack could issue data scan on the file when the provider/Sync engine tries to open a handle to the file to be passed as a parameter to [CfGetPlaceholderRangeInfo](nf-cfapi-cfgetplaceholderrangeinfo.md). Alternatively, a mini filter could block the `FSCTL_HSM_CONTROL` that **CfGetPlaceholderRangeInfo** triggers internally.

The **cldflt** filter is designed to invoke just one `CF_CALLBACK_TYPE_FETCH_DATA` callback per required file range for hydrating the file. As a result of either of above cases, either the data scan is stuck behind the original `CF_CALLBACK_TYPE_FETCH_DATA` or the `CF_CALLBACK_TYPE_FETCH_DATA` is stuck behind the blocked [FSCTL](/openspecs/windows_protocols/ms-fscc/4dc02779-9d95-43f8-bba4-8d4ce4961458). This causes a deadlock in the hydration path.

Hence, this API is needed. It performs the same functionality as [CfGetPlaceholderRangeInfo](nf-cfapi-cfgetplaceholderrangeinfo.md), but communicates to the filter directly using filter message ports bypassing the intermediate IO stack. Therefore, no intermediate mini filter can either obstruct the `CreateFile` or the `FSCTL_HSM_CONTROL`.

Note that the caller always has the `ConnectionKey` obtained via [CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md). It can obtain `TransferKey` via [CfGetTransferKey](nf-cfapi-cfgettransferkey.md) and obtain `FileId` using [GetFileInformationByHandle](/windows/win32/api/fileapi/nf-fileapi-getfileinformationbyhandle). But this approach needs a handle to be opened to the file and hence is no different than using [CfGetPlaceholderRangeInfo](nf-cfapi-cfgetplaceholderrangeinfo.md).

To summarize, when range info is needed from the context of a `CF_CALLBACK_TYPE_FETCH_DATA` callback, this API should be used. In all other cases, including when the provider wants to hydrate the file without being requested by the filter, [CfGetPlaceholderRangeInfo](nf-cfapi-cfgetplaceholderrangeinfo.md) should be used. The platform can’t recognize which API is called in a specific context and hence the onus is on the provider/Sync Engine to do the right thing.

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

[CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md)
