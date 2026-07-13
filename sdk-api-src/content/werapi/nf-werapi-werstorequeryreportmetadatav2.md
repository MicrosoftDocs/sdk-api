---
UID: NF:werapi.WerStoreQueryReportMetadataV2
title: WerStoreQueryReportMetadataV2 function (werapi.h)
description: Retrieves metadata about a Windows Error Reporting (WER) report in the store.
helpviewer_keywords: ["WerStoreQueryReportMetadataV2","WerStoreQueryReportMetadataV2 function [Windows Error Reporting]","wer.werstorequeryreportmetadatav2","werapi/WerStoreQueryReportMetadataV2"]
old-location: wer\werstorequeryreportmetadatav2.htm
tech.root: wer
ms.assetid: ADF6619C-1F3E-4AFF-9E25-4F6F83D1353C
ms.date: 07/26/2023
ms.keywords: WerStoreQueryReportMetadataV2, WerStoreQueryReportMetadataV2 function [Windows Error Reporting], wer.werstorequeryreportmetadatav2, werapi/WerStoreQueryReportMetadataV2
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerStoreQueryReportMetadataV2
 - werapi/WerStoreQueryReportMetadataV2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wer-reporting-l1-1-3.dll
 - ext-ms-win-wer-reporting-l1-1-2.dll
 - wer.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerStoreQueryReportMetadataV2
---

# WerStoreQueryReportMetadataV2 function

## -description

Retrieves metadata about a [Windows Error Reporting](../_wer/index.md) (WER) report in the store.

## -parameters

### -param hReportStore

The error report store (previously retrieved with [WerStoreOpen](/windows/desktop/api/werapi/nf-werapi-werstoreopen)).

### -param pszReportKey

The string identifying which report is being queried (previously retrieved with [WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey) or [WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey)).

### -param pReportMetadata

A pointer to the report store metadata in the form of a [WER_REPORT_METADATA_V2](/windows/desktop/api/werapi/ns-werapi-wer_report_metadata_v2) structure. The field **SizeOfFileNames** should be set to 0 during the first call. The function updates this field with the required size to hold the file names associated with the report. The field **FileNames** should then be allocated with **SizeOfFileNames** bytes and the function should be called again to get all of the file names.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**E_INVALID_ARG**|One of the arguments is not a valid value.|
|**ERROR_INSUFFICIENT_BUFFER**|There is not enough memory available to retrieve the metadata. In this case, the caller should allocate memory of size **SizeOfFileNames** for the **FileNames** field, found in the [WER_REPORT_METADATA_V2](/windows/desktop/api/werapi/ns-werapi-wer_report_metadata_v2) structure, and call the function again.|

## -see-also

[WER_REPORT_METADATA_V2](/windows/desktop/api/werapi/ns-werapi-wer_report_metadata_v2), [WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey), [WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey), [Windows Error Reporting](/windows/desktop/wer)
