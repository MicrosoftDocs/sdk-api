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
 

 

