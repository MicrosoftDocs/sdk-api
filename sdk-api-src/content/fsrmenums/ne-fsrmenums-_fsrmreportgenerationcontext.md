---
UID: NE:fsrmenums._FsrmReportGenerationContext
title: "_FsrmReportGenerationContext"
author: windows-sdk-content
description: Defines the context in which the report is initiated.
old-location: fsrm\fsrmreportgenerationcontext.htm
tech.root: fsrm
ms.assetid: 02e18cc2-7c5e-473f-8a7f-e310bfb1c57d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FsrmReportGenerationContext, FsrmReportGenerationContext enumeration [File Server Resource Manager], FsrmReportGenerationContext_IncidentReport, FsrmReportGenerationContext_InteractiveReport, FsrmReportGenerationContext_ScheduledReport, FsrmReportGenerationContext_Undefined, _FsrmReportGenerationContext, fs.fsrmreportgenerationcontext, fsrm.fsrmreportgenerationcontext, fsrmenums/FsrmReportGenerationContext, fsrmenums/FsrmReportGenerationContext_IncidentReport, fsrmenums/FsrmReportGenerationContext_InteractiveReport, fsrmenums/FsrmReportGenerationContext_ScheduledReport, fsrmenums/FsrmReportGenerationContext_Undefined
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportGenerationContext
product: Windows
targetos: Windows
req.typenames: FsrmReportGenerationContext
req.redist: 
---

# _FsrmReportGenerationContext enumeration


## -description


Defines the context in which the report is initiated.


## -enum-fields




### -field FsrmReportGenerationContext_Undefined

The context is unknown. Do not use this flag.


### -field FsrmReportGenerationContext_ScheduledReport

The report will run as a scheduled report.


### -field FsrmReportGenerationContext_InteractiveReport

The report will run on demand.


### -field FsrmReportGenerationContext_IncidentReport

The report will run in response to a quota or file screen event.


## -see-also




<a href="https://msdn.microsoft.com/74f369d1-2e3d-49a5-bf54-c1b7c13efbd7">IFsrmReportJob::Run</a>



<a href="https://msdn.microsoft.com/90df1a6e-e2e6-4095-8337-61bfd172e203">IFsrmReportManager::GetOutputDirectory</a>



<a href="https://msdn.microsoft.com/5bbc4255-1fed-45c5-bb13-41ee7c47ed56">IFsrmReportManager::SetOutputDirectory</a>
 

 

