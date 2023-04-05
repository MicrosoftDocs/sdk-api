---
UID: NF:cfapi.CfReleaseTransferKey
title: CfReleaseTransferKey function (cfapi.h)
description: Releases a transfer key obtained by CfGetTransferKey.
helpviewer_keywords: ["CfReleaseTransferKey","CfReleaseTransferKey function","cfapi/CfReleaseTransferKey","cloudApi.cfreleasetransferkey"]
old-location: cloudapi\cfreleasetransferkey.htm
tech.root: cloudapi
ms.assetid: 53B40C34-EB1F-445B-B1B3-B539C2FADECE
ms.date: 03/30/2023
ms.keywords: CfReleaseTransferKey, CfReleaseTransferKey function, cfapi/CfReleaseTransferKey, cloudApi.cfreleasetransferkey
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
 - CfReleaseTransferKey
 - cfapi/CfReleaseTransferKey
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
 - CfReleaseTransferKey
---

# CfReleaseTransferKey function

## -description

Releases a transfer key obtained by [CfGetTransferKey](nf-cfapi-cfgettransferkey.md) when it is no longer needed.

## -parameters

### -param FileHandle [in]

The file handle of the placeholder.

### -param TransferKey [in]

An opaque handle to the placeholder.

## -remarks

**CfReleaseTransferKey** has no security requirement.

## -see-also

[CfGetTransferKey](nf-cfapi-cfgettransferkey.md)
