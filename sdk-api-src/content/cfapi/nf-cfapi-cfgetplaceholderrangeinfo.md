---
UID: NF:cfapi.CfGetPlaceholderRangeInfo
title: CfGetPlaceholderRangeInfo function (cfapi.h)
description: Gets range information about a placeholder file or folder.
helpviewer_keywords: ["CfGetPlaceholderRangeInfo","CfGetPlaceholderRangeInfo function","cfapi/CfGetPlaceholderRangeInfo","cloudApi.cfgetplaceholderrangeinfo"]
old-location: cloudapi\cfgetplaceholderrangeinfo.htm
tech.root: cloudapi
ms.assetid: B7FE94BC-DC59-407D-85A6-9657E38975AB
ms.date: 02/27/2023
ms.keywords: CfGetPlaceholderRangeInfo, CfGetPlaceholderRangeInfo function, cfapi/CfGetPlaceholderRangeInfo, cloudApi.cfgetplaceholderrangeinfo
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
 - CfGetPlaceholderRangeInfo
 - cfapi/CfGetPlaceholderRangeInfo
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
 - CfGetPlaceholderRangeInfo
---

# CfGetPlaceholderRangeInfo function

## -description

Gets range information about a placeholder file or folder.

## -parameters

### -param FileHandle [in]

The handle of the placeholder file to be queried.

### -param InfoClass [in]

Types of the range of placeholder data.

### -param StartingOffset [in]

Offset of the starting point of the range of data.

### -param Length [in]

Length of the range of data.

### -param InfoBuffer [out]

Pointer to a buffer that will receive the data. The buffer is an array of `CF_FILE_RANGE` structures, which are offset/length pairs, describing the requested ranges.

### -param InfoBufferLength [in]

The length of `InfoBuffer` in bytes.

### -param ReturnedLength [out, optional]

The length of the returned range of placeholder data in the `InfoBuffer`.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an `HRESULT` error code.

## -remarks

Unlike most placeholder APIs that take a file handle, this one does not modify the file in any way, therefore the file handle only requires READ_ATTRIBUTES access.

## -see-also

[CfGetPlaceholderRangeInfoForHydration](nf-cfapi-cfgetplaceholderrangeinfoforhydration.md)
