---
UID: NF:fsrmreports.IFsrmReportManager.CreateReportJob
title: IFsrmReportManager::CreateReportJob (fsrmreports.h)
description: Creates a report job.
helpviewer_keywords: ["CreateReportJob","CreateReportJob method [File Server Resource Manager]","CreateReportJob method [File Server Resource Manager]","FsrmReportManager class","CreateReportJob method [File Server Resource Manager]","IFsrmReportManager interface","FsrmReportManager class [File Server Resource Manager]","CreateReportJob method","IFsrmReportManager interface [File Server Resource Manager]","CreateReportJob method","IFsrmReportManager.CreateReportJob","IFsrmReportManager::CreateReportJob","fs.ifsrmreportmanager_createreportjob","fsrm.ifsrmreportmanager_createreportjob","fsrmreports/IFsrmReportManager::CreateReportJob"]
old-location: fsrm\ifsrmreportmanager_createreportjob.htm
tech.root: fsrm
ms.assetid: 30274108-a820-409e-ba7c-6971b7726b9b
ms.date: 12/05/2018
ms.keywords: CreateReportJob, CreateReportJob method [File Server Resource Manager], CreateReportJob method [File Server Resource Manager],FsrmReportManager class, CreateReportJob method [File Server Resource Manager],IFsrmReportManager interface, FsrmReportManager class [File Server Resource Manager],CreateReportJob method, IFsrmReportManager interface [File Server Resource Manager],CreateReportJob method, IFsrmReportManager.CreateReportJob, IFsrmReportManager::CreateReportJob, fs.ifsrmreportmanager_createreportjob, fsrm.ifsrmreportmanager_createreportjob, fsrmreports/IFsrmReportManager::CreateReportJob
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportManager::CreateReportJob
 - fsrmreports/IFsrmReportManager::CreateReportJob
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
 - IFsrmReportManager.CreateReportJob
 - FsrmReportManager.CreateReportJob
---

# IFsrmReportManager::CreateReportJob


## -description

Creates a report job.

## -parameters

### -param reportJob [out]

An <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a> interface of the newly created 
      report job object. Use the interface to add reports to the job and run the reports. To add the report job to 
      FSRM, call <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmReportJob::Commit</a> method.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>