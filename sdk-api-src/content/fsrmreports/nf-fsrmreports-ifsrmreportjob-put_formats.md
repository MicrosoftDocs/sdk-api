---
UID: NF:fsrmreports.IFsrmReportJob.put_Formats
title: IFsrmReportJob::put_Formats (fsrmreports.h)
description: Retrieves or sets an array of formats that determine the content format of the reports. (Put)
helpviewer_keywords: ["Formats property [File Server Resource Manager]","Formats property [File Server Resource Manager]","IFsrmReportJob interface","IFsrmReportJob interface [File Server Resource Manager]","Formats property","IFsrmReportJob.Formats","IFsrmReportJob.put_Formats","IFsrmReportJob::Formats","IFsrmReportJob::get_Formats","IFsrmReportJob::put_Formats","fs.ifsrmreportjob_formats","fsrm.ifsrmreportjob_formats","fsrmreports/IFsrmReportJob::Formats","fsrmreports/IFsrmReportJob::get_Formats","fsrmreports/IFsrmReportJob::put_Formats","put_Formats"]
old-location: fsrm\ifsrmreportjob_formats.htm
tech.root: fsrm
ms.assetid: 9d0f7a7f-ad25-4d44-bc11-67da7685142a
ms.date: 12/05/2018
ms.keywords: Formats property [File Server Resource Manager], Formats property [File Server Resource Manager],IFsrmReportJob interface, IFsrmReportJob interface [File Server Resource Manager],Formats property, IFsrmReportJob.Formats, IFsrmReportJob.put_Formats, IFsrmReportJob::Formats, IFsrmReportJob::get_Formats, IFsrmReportJob::put_Formats, fs.ifsrmreportjob_formats, fsrm.ifsrmreportjob_formats, fsrmreports/IFsrmReportJob::Formats, fsrmreports/IFsrmReportJob::get_Formats, fsrmreports/IFsrmReportJob::put_Formats, put_Formats
req.header: fsrmreports.h
req.include-header: 
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportJob::put_Formats
 - fsrmreports/IFsrmReportJob::put_Formats
dev_langs:
 - c++
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

For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-report-job">Defining a Report Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>
