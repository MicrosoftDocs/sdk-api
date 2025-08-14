---
UID: NF:werapi.WerStoreQueryReportMetadataV1
tech.root: wer
title: WerStoreQueryReportMetadataV1
ms.date: 07/21/2023
targetos: Windows
description: Retrieves metadata about a Windows Error Reporting (WER) report in the store.
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
 - WerStoreQueryReportMetadataV1
f1_keywords:
 - WerStoreQueryReportMetadataV1
 - werapi/WerStoreQueryReportMetadataV1
dev_langs:
 - c++
helpviewer_keywords:
 - WerStoreQueryReportMetadataV1
---

# WerStoreQueryReportMetadataV1 function

## -description

Retrieves metadata about a [Windows Error Reporting](../_wer/index.md) (WER) report in the store.

## -parameters

### -param hReportStore

The error report store (previously retrieved with [WerStoreOpen](/windows/desktop/api/werapi/nf-werapi-werstoreopen)).

### -param pszReportKey

The string identifying which report is being queried (previously retrieved with [WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey) or [WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey)).

### -param pReportMetadata

A pointer to the report store metadata in the form of a [WER_REPORT_METADATA_V1](ns-werapi-wer_report_metadata_v1.md) structure.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**E_INVALID_ARG**|One of the arguments is not a valid value.|
|**ERROR_INSUFFICIENT_BUFFER**|There is not enough memory available to retrieve the metadata. |

## -remarks

## -see-also

[WER_REPORT_METADATA_V1](ns-werapi-wer_report_metadata_v1.md), [WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey), [WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey), [Windows Error Reporting](../_wer/index.md)
