---
UID: NF:cfapi.CfGetTransferKey
title: CfGetTransferKey function (cfapi.h)
description: Initiates a transfer of data into a placeholder file or folder.
helpviewer_keywords: ["CfGetTransferKey","CfGetTransferKey function","cfapi/CfGetTransferKey","cloudApi.cfgettransferkey"]
old-location: cloudapi\cfgettransferkey.htm
tech.root: cloudapi
ms.assetid: 07DDC46A-0C10-4677-A4B0-5A0406BBDAB7
ms.date: 03/30/2023
ms.keywords: CfGetTransferKey, CfGetTransferKey function, cfapi/CfGetTransferKey, cloudApi.cfgettransferkey
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
 - CfGetTransferKey
 - cfapi/CfGetTransferKey
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
 - CfGetTransferKey
---

# CfGetTransferKey function

## -description

**CfGetTransferKey** returns *TransferKey*, which is needed to initiate a transfer of data into a placeholder using the [CfExecute](nf-cfapi-cfexecute.md) API.

## -parameters

### -param FileHandle [in]

The file handle of the placeholder.

### -param TransferKey [out]

An opaque handle to the placeholder to be serviced.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

This API is available for sync providers that may wish to proactively initiate a transfer of data into a placeholder, as an alternative to calling [CfHydratePlaceholder](nf-cfapi-cfhydrateplaceholder.md). **CfGetTransferKey** returns the same *TransferKey* that a fetch data callback would have returned. The sync provider can then pass the *TransferKey* in subsequent calls to the [CfExecute](nf-cfapi-cfexecute.md) API. In this way, the transfer of data is driven by the sync provider rather than the filter.

A sync provider should have **READ_DATA** or **WRITE_DAC** access to the file whose transfer key is to be obtained or **CfGetTransferKey** will be failed with **HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED)**.

The *TransferKey* is valid as long as the *FileHandle* used to obtain it remains open. The sync provider must pass the *TransferKey* to [CfExecute](nf-cfapi-cfexecute.md) to perform the desired operation on the placeholder file or folder. When a *TransferKey* is no longer being used, it must be released using [CfReleaseTransferKey](nf-cfapi-cfreleasetransferkey.md).

## -see-also

[CfHydratePlaceholder](nf-cfapi-cfhydrateplaceholder.md)

[CfExecute](nf-cfapi-cfexecute.md)

[CfReleaseTransferKey](nf-cfapi-cfreleasetransferkey.md)
