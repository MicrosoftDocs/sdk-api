---
UID: NF:fsrmreports.IFsrmFileManagementJobManager.EnumFileManagementJobs
title: IFsrmFileManagementJobManager::EnumFileManagementJobs (fsrmreports.h)
description: Enumerates the list of existing file management jobs.
helpviewer_keywords: ["EnumFileManagementJobs","EnumFileManagementJobs method [File Server Resource Manager]","EnumFileManagementJobs method [File Server Resource Manager]","FsrmFileManagementJobManager class","EnumFileManagementJobs method [File Server Resource Manager]","IFsrmFileManagementJobManager interface","FsrmFileManagementJobManager class [File Server Resource Manager]","EnumFileManagementJobs method","IFsrmFileManagementJobManager interface [File Server Resource Manager]","EnumFileManagementJobs method","IFsrmFileManagementJobManager.EnumFileManagementJobs","IFsrmFileManagementJobManager::EnumFileManagementJobs","fs.ifsrmfilemanagementjobmanager_enumfilemanagementjobs","fsrm.ifsrmfilemanagementjobmanager_enumfilemanagementjobs","fsrmreports/IFsrmFileManagementJobManager::EnumFileManagementJobs"]
old-location: fsrm\ifsrmfilemanagementjobmanager_enumfilemanagementjobs.htm
tech.root: fsrm
ms.assetid: 4af6f794-d9d4-4e03-9cd5-a4d8769888ca
ms.date: 12/05/2018
ms.keywords: EnumFileManagementJobs, EnumFileManagementJobs method [File Server Resource Manager], EnumFileManagementJobs method [File Server Resource Manager],FsrmFileManagementJobManager class, EnumFileManagementJobs method [File Server Resource Manager],IFsrmFileManagementJobManager interface, FsrmFileManagementJobManager class [File Server Resource Manager],EnumFileManagementJobs method, IFsrmFileManagementJobManager interface [File Server Resource Manager],EnumFileManagementJobs method, IFsrmFileManagementJobManager.EnumFileManagementJobs, IFsrmFileManagementJobManager::EnumFileManagementJobs, fs.ifsrmfilemanagementjobmanager_enumfilemanagementjobs, fsrm.ifsrmfilemanagementjobmanager_enumfilemanagementjobs, fsrmreports/IFsrmFileManagementJobManager::EnumFileManagementJobs
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmFileManagementJobManager::EnumFileManagementJobs
 - fsrmreports/IFsrmFileManagementJobManager::EnumFileManagementJobs
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
 - IFsrmFileManagementJobManager.EnumFileManagementJobs
 - FsrmFileManagementJobManager.EnumFileManagementJobs
---

# IFsrmFileManagementJobManager::EnumFileManagementJobs


## -description

Enumerates the list of existing file management jobs.

## -parameters

### -param options [in]

One or more options to use when enumerating the management jobs. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  This parameter must be set to either <b>FsrmEnumOptions_IncludeClusterNodes</b> or <b>FsrmEnumOptions_None</b> for this method.</div>
<div> </div>

### -param fileManagementJobs [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a collection of file management jobs.  The variant type of each item in the collection is <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant to get an <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a> interface to the job.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilemanagementjobmanager">FsrmFileManagementJobManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjobmanager">IFsrmFileManagementJobManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-getfilemanagementjob">IFsrmFileManagementJobManager::GetFileManagementJob</a>