---
UID: NF:fsrmreports.IFsrmReportJob.CreateReport
title: IFsrmReportJob::CreateReport
author: windows-sdk-content
description: Creates a new report object of the specified type.
old-location: fsrm\ifsrmreportjob_createreport.htm
tech.root: fsrm
ms.assetid: 484941d1-726c-4765-8652-bcb378f277b4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateReport, CreateReport method [File Server Resource Manager], CreateReport method [File Server Resource Manager],IFsrmReportJob interface, IFsrmReportJob interface [File Server Resource Manager],CreateReport method, IFsrmReportJob.CreateReport, IFsrmReportJob::CreateReport, fs.ifsrmreportjob_createreport, fsrm.ifsrmreportjob_createreport, fsrmreports/IFsrmReportJob::CreateReport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportJob.CreateReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmReportJob::CreateReport


## -description


Creates a new report object of the specified type.


## -parameters




### -param reportType [in]

Type of report to generate. For possible values, see the<a href="https://msdn.microsoft.com/6fb5cb02-371b-4d07-9f13-d0409d5835d4">FsrmReportType</a> enumeration.

Note that the job can contain only one report of each type.


### -param report [out]

An <a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a> interface to the newly created report. Use the interface to configure the report.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>
 

 

