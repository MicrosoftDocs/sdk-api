---
UID: NF:fsrmreports.IFsrmReportJob.CreateReport
title: IFsrmReportJob::CreateReport (fsrmreports.h)
description: Creates a new report object of the specified type.
helpviewer_keywords: ["CreateReport","CreateReport method [File Server Resource Manager]","CreateReport method [File Server Resource Manager]","IFsrmReportJob interface","IFsrmReportJob interface [File Server Resource Manager]","CreateReport method","IFsrmReportJob.CreateReport","IFsrmReportJob::CreateReport","fs.ifsrmreportjob_createreport","fsrm.ifsrmreportjob_createreport","fsrmreports/IFsrmReportJob::CreateReport"]
old-location: fsrm\ifsrmreportjob_createreport.htm
tech.root: fsrm
ms.assetid: 484941d1-726c-4765-8652-bcb378f277b4
ms.date: 12/05/2018
ms.keywords: CreateReport, CreateReport method [File Server Resource Manager], CreateReport method [File Server Resource Manager],IFsrmReportJob interface, IFsrmReportJob interface [File Server Resource Manager],CreateReport method, IFsrmReportJob.CreateReport, IFsrmReportJob::CreateReport, fs.ifsrmreportjob_createreport, fsrm.ifsrmreportjob_createreport, fsrmreports/IFsrmReportJob::CreateReport
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
 - IFsrmReportJob::CreateReport
 - fsrmreports/IFsrmReportJob::CreateReport
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
 - IFsrmReportJob.CreateReport
---

# IFsrmReportJob::CreateReport


## -description

Creates a new report object of the specified type.

## -parameters

### -param reportType [in]

Type of report to generate. For possible values, see the<a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreporttype">FsrmReportType</a> enumeration.

Note that the job can contain only one report of each type.

### -param report [out]

An <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreport">IFsrmReport</a> interface to the newly created report. Use the interface to configure the report.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>