---
UID: NF:cfapi.CfHydratePlaceholder
title: CfHydratePlaceholder function (cfapi.h)
description: Hydrates a placeholder file by ensuring that the specified byte range is present on-disk in the placeholder. This is valid for files only.
helpviewer_keywords: ["CfHydratePlaceholder","CfHydratePlaceholder function","cfapi/CfHydratePlaceholder","cloudApi.cfhydrateplaceholder"]
old-location: cloudapi\cfhydrateplaceholder.htm
tech.root: cloudapi
ms.assetid: 4FFD7580-BF59-48D0-B6D7-516559914096
ms.date: 03/30/2023
ms.keywords: CfHydratePlaceholder, CfHydratePlaceholder function, cfapi/CfHydratePlaceholder, cloudApi.cfhydrateplaceholder
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
 - CfHydratePlaceholder
 - cfapi/CfHydratePlaceholder
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
 - CfHydratePlaceholder
---

# CfHydratePlaceholder function

## -description

Hydrates a placeholder file by ensuring that the specified byte range is present on-disk in the placeholder. This is valid for files only.

## -parameters

### -param FileHandle [in]

Handle of the placeholder file to be hydrated. An attribute or no-access handle is sufficient.

### -param StartingOffset [in]

The starting point offset of the placeholder file data.

### -param Length [in]

The length, in bytes, of the placeholder file whose data must be available locally on the disk after the API completes successfully. A length of `CF_EOF` (defined as -1) signifies end of file. For any subrange that is not present in the placeholder, the platform will fetch the data from the sync provider and store it on disk in the placeholder.

### -param HydrateFlags [in]

The placeholder hydration flags. *HydrateFlags* must be set to **CF_HYDRATE_FLAG_NONE**.

### -param Overlapped [in, out, optional]

When specified and combined with an asynchronous *FileHandle*, *Overlapped* allows the platform to perform the **CfHydratePlaceholder** call asynchronously. See the [Remarks](#-remarks) for more details.

If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

The caller must have **READ_DATA** or **WRITE_DAC** access to the placeholder to be hydrated.

If the API returns **HRESULT_FROM_WIN32(ERROR_IO_PENDING)** when using *Overlapped* asynchronously, the caller can then wait using [GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).

## -see-also

[GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)
