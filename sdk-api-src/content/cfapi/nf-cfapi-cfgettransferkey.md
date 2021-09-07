---
UID: NF:cfapi.CfGetTransferKey
title: CfGetTransferKey function (cfapi.h)
description: Initiates a transfer of data into a placeholder file or folder.
helpviewer_keywords: ["CfGetTransferKey","CfGetTransferKey function","cfapi/CfGetTransferKey","cloudApi.cfgettransferkey"]
old-location: cloudapi\cfgettransferkey.htm
tech.root: cloudapi
ms.assetid: 07DDC46A-0C10-4677-A4B0-5A0406BBDAB7
ms.date: 12/05/2018
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

Initiates a transfer of data into a placeholder file or folder.

## -parameters

### -param FileHandle [in]

The file handle of the placeholder.

### -param TransferKey [out]

An opaque handle to the placeholder to be serviced.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>CfGetTransferKey</b> is used as an alternative to <a href="/windows/desktop/api/cfapi/nf-cfapi-cfhydrateplaceholder">CfHydratePlaceholder</a> to proactively initiate data transfer into a placeholder.

A sync provider should have READ_DATA or WRITE_DAC access to the file whose transfer key is to be obtained or <b>CfGetTransferKey</b> will be failed with HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED).

The <i>TransferKey</i> is valid as long as the <i>FileHandle</i> used to obtain it remains open. The sync provider must pass the <i>TransferKey</i> to <a href="/windows/desktop/api/cfapi/nf-cfapi-cfexecute">CfExecute</a> to perform the desired operation on the placeholder file or folder.  When a <i>TransferKey</i> is no longer being used, it must be released using <a href="/windows/desktop/api/cfapi/nf-cfapi-cfreleasetransferkey">CfReleaseTransferKey</a>.