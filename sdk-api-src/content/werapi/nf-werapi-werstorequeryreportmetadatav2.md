---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

