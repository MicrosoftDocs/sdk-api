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

# IFsrmReportJob::put_Formats


## -description


Retrieves or sets an array of formats that determine the content format of the reports.

This property is read/write.


## -parameters


## -remarks



Each report in the job is generated in each of the specified formats.

The file name extension is based on the format. The extension for DHTML is 
    ".html", the extension for HTML is ".htm", the 
    extension for TXT is ".txt", the extension for CSV is 
    ".csv", and the extension for XML is 
    ".xml".

If the report type is <b>FsrmReportType_ExportReport</b>, you can specify only the 
    <b>FsrmReportFormat_Csv</b> and <b>FsrmReportFormat_Xml</b> formats. 
    The report is not run if one or both of these formats are not specified. Other formats are ignored.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/a91c4fe7-ec8c-4d2b-b565-559e16668c87">Defining a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>
 

 

