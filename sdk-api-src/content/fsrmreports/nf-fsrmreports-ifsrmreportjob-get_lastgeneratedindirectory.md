---
UID: NF:fsrmreports.IFsrmReportJob.get_LastGeneratedInDirectory
title: IFsrmReportJob::get_LastGeneratedInDirectory (fsrmreports.h)
author: windows-sdk-content
description: Retrieves the local directory path where the reports were stored the last time the reports were run.
old-location: fsrm\ifsrmreportjob_lastgeneratedindirectory.htm
tech.root: fsrm
ms.assetid: b72ce871-41e0-4321-8c9c-0ae77a02c7ff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],LastGeneratedInDirectory property, IFsrmReportJob.LastGeneratedInDirectory, IFsrmReportJob.get_LastGeneratedInDirectory, IFsrmReportJob::LastGeneratedInDirectory, IFsrmReportJob::get_LastGeneratedInDirectory, LastGeneratedInDirectory property [File Server Resource Manager], LastGeneratedInDirectory property [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_lastgeneratedindirectory, fsrm.ifsrmreportjob_lastgeneratedindirectory, fsrmreports/IFsrmReportJob::LastGeneratedInDirectory, fsrmreports/IFsrmReportJob::get_LastGeneratedInDirectory, get_LastGeneratedInDirectory
ms.topic: method
f1_keywords: 
 - "fsrmreports/IFsrmReportJob.LastGeneratedInDirectory"
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
 - IFsrmReportJob.LastGeneratedInDirectory
 - IFsrmReportJob.get_LastGeneratedInDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmReportJob::get_LastGeneratedInDirectory


## -description


Retrieves the local directory path where the reports were stored the last time the reports were run.

This property is read-only.


## -parameters


## -remarks



If the reports failed, this is the path where the reports would have been stored. The directory may contain reports that completed successfully before the failure occurred.


#### Examples

For an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/running-a-report-job">Running a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setoutputdirectory">IFsrmReportManager::SetOutputDirectory</a>
 

 

