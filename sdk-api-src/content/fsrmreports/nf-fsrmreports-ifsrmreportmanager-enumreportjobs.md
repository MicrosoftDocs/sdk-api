---
UID: NF:fsrmreports.IFsrmReportManager.EnumReportJobs
title: IFsrmReportManager::EnumReportJobs (fsrmreports.h)
description: Enumerates the report jobs.
helpviewer_keywords: ["EnumReportJobs","EnumReportJobs method [File Server Resource Manager]","EnumReportJobs method [File Server Resource Manager]","FsrmReportManager class","EnumReportJobs method [File Server Resource Manager]","IFsrmReportManager interface","FsrmReportManager class [File Server Resource Manager]","EnumReportJobs method","IFsrmReportManager interface [File Server Resource Manager]","EnumReportJobs method","IFsrmReportManager.EnumReportJobs","IFsrmReportManager::EnumReportJobs","fs.ifsrmreportmanager_enumreportjobs","fsrm.ifsrmreportmanager_enumreportjobs","fsrmreports/IFsrmReportManager::EnumReportJobs"]
old-location: fsrm\ifsrmreportmanager_enumreportjobs.htm
tech.root: fsrm
ms.assetid: af66beb6-e82c-47e6-8658-da9702041053
ms.date: 12/05/2018
ms.keywords: EnumReportJobs, EnumReportJobs method [File Server Resource Manager], EnumReportJobs method [File Server Resource Manager],FsrmReportManager class, EnumReportJobs method [File Server Resource Manager],IFsrmReportManager interface, FsrmReportManager class [File Server Resource Manager],EnumReportJobs method, IFsrmReportManager interface [File Server Resource Manager],EnumReportJobs method, IFsrmReportManager.EnumReportJobs, IFsrmReportManager::EnumReportJobs, fs.ifsrmreportmanager_enumreportjobs, fsrm.ifsrmreportmanager_enumreportjobs, fsrmreports/IFsrmReportManager::EnumReportJobs
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
 - IFsrmReportManager::EnumReportJobs
 - fsrmreports/IFsrmReportManager::EnumReportJobs
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
 - IFsrmReportManager.EnumReportJobs
 - FsrmReportManager.EnumReportJobs
---

# IFsrmReportManager::EnumReportJobs


## -description

Enumerates the report jobs.

## -parameters

### -param options [in]

The options to use when enumerating the report jobs. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmEnumOptions_Asynchronous</b> option is not supported for this 
       method.</div>
<div> </div>

### -param reportJobs [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a 
      collection of the report jobs. The collection is empty if no report jobs.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member to get the 
       <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a> interface.

The collection can contain committed and uncommitted report jobs. For an uncommitted report job to be 
       included in the collection, the running status of the job must be 
       <b>FsrmReportRunningStatus_Queued</b> or 
       <b>FsrmReportRunningStatus_Running</b>.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>