---
UID: NF:fsrmreports.IFsrmReportJob.get_Formats
title: IFsrmReportJob::get_Formats
author: windows-sdk-content
description: Retrieves or sets an array of formats that determine the content format of the reports.
old-location: fsrm\ifsrmreportjob_formats.htm
old-project: fsrm
ms.assetid: 9d0f7a7f-ad25-4d44-bc11-67da7685142a
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: Formats property [File Server Resource Manager], Formats property [File Server Resource Manager],IFsrmReportJob interface, IFsrmReportJob interface [File Server Resource Manager],Formats property, IFsrmReportJob.Formats, IFsrmReportJob.get_Formats, IFsrmReportJob::Formats, IFsrmReportJob::get_Formats, IFsrmReportJob::put_Formats, fs.ifsrmreportjob_formats, fsrm.ifsrmreportjob_formats, fsrmreports/IFsrmReportJob::Formats, fsrmreports/IFsrmReportJob::get_Formats, fsrmreports/IFsrmReportJob::put_Formats, get_Formats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmreports.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportJob.Formats
 - IFsrmReportJob.get_Formats
 - IFsrmReportJob.put_Formats
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportJob::get_Formats


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
 

 

