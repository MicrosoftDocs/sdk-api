---
UID: NF:fsrmreports.IFsrmReportJob.EnumReports
title: IFsrmReportJob::EnumReports (fsrmreports.h)
description: Enumerates all the reports configured for this report job.
helpviewer_keywords: ["EnumReports","EnumReports method [File Server Resource Manager]","EnumReports method [File Server Resource Manager]","IFsrmReportJob interface","IFsrmReportJob interface [File Server Resource Manager]","EnumReports method","IFsrmReportJob.EnumReports","IFsrmReportJob::EnumReports","fs.ifsrmreportjob_enumreports","fsrm.ifsrmreportjob_enumreports","fsrmreports/IFsrmReportJob::EnumReports"]
old-location: fsrm\ifsrmreportjob_enumreports.htm
tech.root: fsrm
ms.assetid: a1292084-f1b5-43eb-9b59-fa2f3f99557d
ms.date: 12/05/2018
ms.keywords: EnumReports, EnumReports method [File Server Resource Manager], EnumReports method [File Server Resource Manager],IFsrmReportJob interface, IFsrmReportJob interface [File Server Resource Manager],EnumReports method, IFsrmReportJob.EnumReports, IFsrmReportJob::EnumReports, fs.ifsrmreportjob_enumreports, fsrm.ifsrmreportjob_enumreports, fsrmreports/IFsrmReportJob::EnumReports
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
 - IFsrmReportJob::EnumReports
 - fsrmreports/IFsrmReportJob::EnumReports
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
 - IFsrmReportJob.EnumReports
---

# IFsrmReportJob::EnumReports


## -description

Enumerates all the reports configured for this report job.

## -parameters

### -param reports [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a collection of reports. The collection is empty if no reports are defined for the job.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member to get the <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreport">IFsrmReport</a> interface.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>