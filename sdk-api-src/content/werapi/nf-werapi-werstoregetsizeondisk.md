---
UID: NF:werapi.WerStoreGetSizeOnDisk
tech.root: wer
title: WerStoreGetSizeOnDisk
ms.date: 07/21/2023
targetos: Windows
description: Gets the size of the Windows Error Reporting (WER) error report store, in bytes.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: werapi.h
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
 - HeaderDef
api_location:
 - ext-ms-win-wer-reporting-l1-1-3.dll
 - ext-ms-win-wer-reporting-l1-1-2.dll
 - ext-ms-win-wer-reporting-l1-1-1.dll
 - werapi.h
api_name:
 - WerStoreGetSizeOnDisk
f1_keywords:
 - WerStoreGetSizeOnDisk
 - werapi/WerStoreGetSizeOnDisk
dev_langs:
 - c++
helpviewer_keywords:
 - WerStoreGetSizeOnDisk
---

# WerStoreGetSizeOnDisk function

## -description

Gets the size of the [Windows Error Reporting](../_wer/index.md) (WER) error report store, in bytes.

## -parameters

### -param hReportStore

The error report store (previously retrieved with [WerStoreOpen](/windows/desktop/api/werapi/nf-werapi-werstoreopen)).

### -param pqwSizeInBytes

The error report store size, in bytes.

## -returns

|Return code|Description|
|--- |--- |
|**E_INVALID_ARG**|One of the arguments is not a valid value.|
|**ERROR_NO_MORE_FILES**|There are no more error reports in the store.|

## -remarks

## -see-also
