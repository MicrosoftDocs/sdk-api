---
UID: NF:werapi.WerStoreQueryReportMetadataV2
title: WerStoreQueryReportMetadataV2 function
author: windows-sdk-content
description: Retrieves metadata about a report in the store.
old-location: wer\werstorequeryreportmetadatav2.htm
old-project: wer
ms.assetid: ADF6619C-1F3E-4AFF-9E25-4F6F83D1353C
ms.author: windowssdkdev
ms.date: 03/22/2018
ms.keywords: WerStoreQueryReportMetadataV2, WerStoreQueryReportMetadataV2 function [Windows Error Reporting], wer.werstorequeryreportmetadatav2, werapi/WerStoreQueryReportMetadataV2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wer.dll
-	API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
-	KernelBase.dll
api_name:
-	WerStoreQueryReportMetadataV2
product: Windows
targetos: Windows
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerStoreQueryReportMetadataV2 function


## -description


Retrieves metadata about a report in the store.


## -parameters




### -param hReportStore

TBD


### -param pszReportKey

TBD


### -param pReportMetadata

TBD




#### - metadata

A pointer to the report store metadata in the form of a <a href="https://msdn.microsoft.com/037170B1-B2DF-402F-A9E6-48C7693C9A93">WER_REPORT_METADATA_V2</a> structure. The field <b>SizeOfFileNames</b> should be set to 0 during the first call. The function updates this field with the required size to hold the file names associated with the report. The field <b>FileNames</b> should then be allocated with <b>SizeOfFileNames</b> bytes and the function should be called again to get all of the file names.


#### - reportKey

The string identifying which report is being queried (previously retrieved with <a href="https://msdn.microsoft.com/E4732B60-BFBE-4916-83A6-5F031D267913">WerStoreGetFirstReportKey</a> or <a href="https://msdn.microsoft.com/781D54A9-6F51-445E-89A8-A0C944081B81">WerStoreGetNextReportKey</a>).


#### - store

The error report store (previously retrieved with <a href="https://msdn.microsoft.com/FA7E0EC6-00F1-45E2-BE34-D732965FBA15">WerStoreOpen</a>).


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
There is not enough memory available to retrieve the metadata. In this case, the caller should allocate memory of size <b>SizeOfFileNames</b> for the <b>FileNames</b> field, found in the <a href="https://msdn.microsoft.com/037170B1-B2DF-402F-A9E6-48C7693C9A93">WER_REPORT_METADATA_V2</a> structure, and call the function again. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/037170B1-B2DF-402F-A9E6-48C7693C9A93">WER_REPORT_METADATA_V2</a>



<a href="https://msdn.microsoft.com/E4732B60-BFBE-4916-83A6-5F031D267913">WerStoreGetFirstReportKey</a>



<a href="https://msdn.microsoft.com/781D54A9-6F51-445E-89A8-A0C944081B81">WerStoreGetNextReportKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

