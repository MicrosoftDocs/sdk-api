---
UID: NF:cfapi.CfHydratePlaceholder
title: CfHydratePlaceholder function (cfapi.h)
description: Hydrates a placeholder file by ensuring that the specified byte range is present on-disk in the placeholder. This is valid for files only.
helpviewer_keywords: ["CfHydratePlaceholder","CfHydratePlaceholder function","cfapi/CfHydratePlaceholder","cloudApi.cfhydrateplaceholder"]
old-location: cloudapi\cfhydrateplaceholder.htm
tech.root: cloudapi
ms.assetid: 4FFD7580-BF59-48D0-B6D7-516559914096
ms.date: 12/05/2018
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

The length, in bytes,  of the placeholder file whose data must be available locally on the disk after the API completes successfully. A length of -1 signifies end of file.

### -param HydrateFlags [in]

Placeholder hydration flags.

### -param Overlapped [in, out, optional]

When specified and combined with an asynchronous <i>FileHandle</i>, <i>Overlapped</i> allows the platform to perform the <b>CfHydratePlaceholder</b> call asynchronously. See the Remarks for more details.

If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.

## -returns

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

The caller must have READ_DATA or WRITE_DAC access to the placeholder to be hydrated. 

If the API returns HRESULT_FROM_WIN32(ERROR_IO_PENDING) when using <i>Overlapped</i> asynchronously, the caller can then wait using <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>.