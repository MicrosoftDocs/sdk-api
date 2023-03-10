---
UID: NE:fsrmenums._FsrmReportGenerationContext
title: FsrmReportGenerationContext (fsrmenums.h)
description: Defines the context in which the report is initiated.
helpviewer_keywords: ["FsrmReportGenerationContext","FsrmReportGenerationContext enumeration [File Server Resource Manager]","FsrmReportGenerationContext_IncidentReport","FsrmReportGenerationContext_InteractiveReport","FsrmReportGenerationContext_ScheduledReport","FsrmReportGenerationContext_Undefined","fs.fsrmreportgenerationcontext","fsrm.fsrmreportgenerationcontext","fsrmenums/FsrmReportGenerationContext","fsrmenums/FsrmReportGenerationContext_IncidentReport","fsrmenums/FsrmReportGenerationContext_InteractiveReport","fsrmenums/FsrmReportGenerationContext_ScheduledReport","fsrmenums/FsrmReportGenerationContext_Undefined"]
old-location: fsrm\fsrmreportgenerationcontext.htm
tech.root: fsrm
ms.assetid: 02e18cc2-7c5e-473f-8a7f-e310bfb1c57d
ms.date: 12/05/2018
ms.keywords: FsrmReportGenerationContext, FsrmReportGenerationContext enumeration [File Server Resource Manager], FsrmReportGenerationContext_IncidentReport, FsrmReportGenerationContext_InteractiveReport, FsrmReportGenerationContext_ScheduledReport, FsrmReportGenerationContext_Undefined, fs.fsrmreportgenerationcontext, fsrm.fsrmreportgenerationcontext, fsrmenums/FsrmReportGenerationContext, fsrmenums/FsrmReportGenerationContext_IncidentReport, fsrmenums/FsrmReportGenerationContext_InteractiveReport, fsrmenums/FsrmReportGenerationContext_ScheduledReport, fsrmenums/FsrmReportGenerationContext_Undefined
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmReportGenerationContext
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmReportGenerationContext
 - fsrmenums/_FsrmReportGenerationContext
 - FsrmReportGenerationContext
 - fsrmenums/FsrmReportGenerationContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportGenerationContext
---

# FsrmReportGenerationContext enumeration


## -description

Defines the context in which the report is initiated.

## -enum-fields

### -field FsrmReportGenerationContext_Undefined:1

The context is unknown. Do not use this flag.

### -field FsrmReportGenerationContext_ScheduledReport:2

The report will run as a scheduled report.

### -field FsrmReportGenerationContext_InteractiveReport:3

The report will run on demand.

### -field FsrmReportGenerationContext_IncidentReport:4

The report will run in response to a quota or file screen event.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-run">IFsrmReportJob::Run</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getoutputdirectory">IFsrmReportManager::GetOutputDirectory</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setoutputdirectory">IFsrmReportManager::SetOutputDirectory</a>
