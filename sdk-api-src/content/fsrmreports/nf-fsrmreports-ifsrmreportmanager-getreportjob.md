---
UID: NF:fsrmreports.IFsrmReportManager.GetReportJob
title: IFsrmReportManager::GetReportJob (fsrmreports.h)
description: Retrieves the specified report job.
helpviewer_keywords: ["FsrmReportManager class [File Server Resource Manager]","GetReportJob method","GetReportJob","GetReportJob method [File Server Resource Manager]","GetReportJob method [File Server Resource Manager]","FsrmReportManager class","GetReportJob method [File Server Resource Manager]","IFsrmReportManager interface","IFsrmReportManager interface [File Server Resource Manager]","GetReportJob method","IFsrmReportManager.GetReportJob","IFsrmReportManager::GetReportJob","fs.ifsrmreportmanager_getreportjob","fsrm.ifsrmreportmanager_getreportjob","fsrmreports/IFsrmReportManager::GetReportJob"]
old-location: fsrm\ifsrmreportmanager_getreportjob.htm
tech.root: fsrm
ms.assetid: 60a1387f-a25f-4026-a582-71981c26dd1b
ms.date: 12/05/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],GetReportJob method, GetReportJob, GetReportJob method [File Server Resource Manager], GetReportJob method [File Server Resource Manager],FsrmReportManager class, GetReportJob method [File Server Resource Manager],IFsrmReportManager interface, IFsrmReportManager interface [File Server Resource Manager],GetReportJob method, IFsrmReportManager.GetReportJob, IFsrmReportManager::GetReportJob, fs.ifsrmreportmanager_getreportjob, fsrm.ifsrmreportmanager_getreportjob, fsrmreports/IFsrmReportManager::GetReportJob
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
 - IFsrmReportManager::GetReportJob
 - fsrmreports/IFsrmReportManager::GetReportJob
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
 - IFsrmReportManager.GetReportJob
 - FsrmReportManager.GetReportJob
---

# IFsrmReportManager::GetReportJob


## -description

Retrieves the specified report job.

## -parameters

### -param taskName [in]

The task name that identifies the report job to retrieve. The string is limited to 230 characters.

### -param reportJob [out]

An <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a> interface to the retrieved job.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>