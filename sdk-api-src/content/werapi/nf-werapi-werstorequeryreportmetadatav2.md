---
UID: NF:werapi.WerStoreQueryReportMetadataV2
title: WerStoreQueryReportMetadataV2 function (werapi.h)
description: Retrieves metadata about a report in the store.
helpviewer_keywords: ["WerStoreQueryReportMetadataV2","WerStoreQueryReportMetadataV2 function [Windows Error Reporting]","wer.werstorequeryreportmetadatav2","werapi/WerStoreQueryReportMetadataV2"]
old-location: wer\werstorequeryreportmetadatav2.htm
tech.root: wer
ms.assetid: ADF6619C-1F3E-4AFF-9E25-4F6F83D1353C
ms.date: 12/05/2018
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
 - wer.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerStoreQueryReportMetadataV2
---

# WerStoreQueryReportMetadataV2 function


## -description

Retrieves metadata about a report in the store.

## -parameters

### -param hReportStore

The error report store (previously retrieved with <a href="/windows/desktop/api/werapi/nf-werapi-werstoreopen">WerStoreOpen</a>).

### -param pszReportKey

The string identifying which report is being queried (previously retrieved with <a href="/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey">WerStoreGetFirstReportKey</a> or <a href="/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey">WerStoreGetNextReportKey</a>).

### -param pReportMetadata

A pointer to the report store metadata in the form of a <a href="/windows/desktop/api/werapi/ns-werapi-wer_report_metadata_v2">WER_REPORT_METADATA_V2</a> structure. The field <b>SizeOfFileNames</b> should be set to 0 during the first call. The function updates this field with the required size to hold the file names associated with the report. The field <b>FileNames</b> should then be allocated with <b>SizeOfFileNames</b> bytes and the function should be called again to get all of the file names.

## -returns

This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to retrieve the metadata. In this case, the caller should allocate memory of size <b>SizeOfFileNames</b> for the <b>FileNames</b> field, found in the <a href="/windows/desktop/api/werapi/ns-werapi-wer_report_metadata_v2">WER_REPORT_METADATA_V2</a> structure, and call the function again. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/ns-werapi-wer_report_metadata_v2">WER_REPORT_METADATA_V2</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey">WerStoreGetFirstReportKey</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey">WerStoreGetNextReportKey</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>