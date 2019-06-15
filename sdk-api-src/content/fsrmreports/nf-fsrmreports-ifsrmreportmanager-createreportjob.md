---
UID: NF:fsrmreports.IFsrmReportManager.CreateReportJob
title: IFsrmReportManager::CreateReportJob (fsrmreports.h)
author: windows-sdk-content
description: Creates a report job.
old-location: fsrm\ifsrmreportmanager_createreportjob.htm
tech.root: fsrm
ms.assetid: 30274108-a820-409e-ba7c-6971b7726b9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateReportJob, CreateReportJob method [File Server Resource Manager], CreateReportJob method [File Server Resource Manager],FsrmReportManager class, CreateReportJob method [File Server Resource Manager],IFsrmReportManager interface, FsrmReportManager class [File Server Resource Manager],CreateReportJob method, IFsrmReportManager interface [File Server Resource Manager],CreateReportJob method, IFsrmReportManager.CreateReportJob, IFsrmReportManager::CreateReportJob, fs.ifsrmreportmanager_createreportjob, fsrm.ifsrmreportmanager_createreportjob, fsrmreports/IFsrmReportManager::CreateReportJob
ms.topic: method
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
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
 - IFsrmReportManager.CreateReportJob
 - FsrmReportManager.CreateReportJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmReportManager::CreateReportJob


## -description


Creates a report job.


## -parameters




### -param reportJob [out]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a> interface of the newly created 
      report job object. Use the interface to add reports to the job and run the reports. To add the report job to 
      FSRM, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmReportJob::Commit</a> method.


## -returns



The method returns the following return values.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>
 

 

