---
UID: NF:fsrmpipeline.IFsrmClassificationManager.get_ClassificationRunningStatus
title: IFsrmClassificationManager::get_ClassificationRunningStatus (fsrmpipeline.h)
description: The running status of the classification.
helpviewer_keywords: ["ClassificationRunningStatus property [File Server Resource Manager]","ClassificationRunningStatus property [File Server Resource Manager]","FsrmClassificationManager class","ClassificationRunningStatus property [File Server Resource Manager]","IFsrmClassificationManager interface","ClassificationRunningStatus property [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","ClassificationRunningStatus property","IFsrmClassificationManager interface [File Server Resource Manager]","ClassificationRunningStatus property","IFsrmClassificationManager.ClassificationRunningStatus","IFsrmClassificationManager.get_ClassificationRunningStatus","IFsrmClassificationManager2 interface [File Server Resource Manager]","ClassificationRunningStatus property","IFsrmClassificationManager2.ClassificationRunningStatus","IFsrmClassificationManager2::get_ClassificationRunningStatus","IFsrmClassificationManager::ClassificationRunningStatus","IFsrmClassificationManager::get_ClassificationRunningStatus","fs.ifsrmclassificationmanager_classificationrunningstatus","fsrm.ifsrmclassificationmanager_classificationrunningstatus","fsrmpipeline/IFsrmClassificationManager2::ClassificationRunningStatus","fsrmpipeline/IFsrmClassificationManager2::get_ClassificationRunningStatus","fsrmpipeline/IFsrmClassificationManager::ClassificationRunningStatus","fsrmpipeline/IFsrmClassificationManager::get_ClassificationRunningStatus","get_ClassificationRunningStatus"]
old-location: fsrm\ifsrmclassificationmanager_classificationrunningstatus.htm
tech.root: fsrm
ms.assetid: f0a10671-9383-4935-b773-31f047732e27
ms.date: 12/05/2018
ms.keywords: ClassificationRunningStatus property [File Server Resource Manager], ClassificationRunningStatus property [File Server Resource Manager],FsrmClassificationManager class, ClassificationRunningStatus property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationRunningStatus property [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassificationRunningStatus property, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationRunningStatus property, IFsrmClassificationManager.ClassificationRunningStatus, IFsrmClassificationManager.get_ClassificationRunningStatus, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationRunningStatus property, IFsrmClassificationManager2.ClassificationRunningStatus, IFsrmClassificationManager2::get_ClassificationRunningStatus, IFsrmClassificationManager::ClassificationRunningStatus, IFsrmClassificationManager::get_ClassificationRunningStatus, fs.ifsrmclassificationmanager_classificationrunningstatus, fsrm.ifsrmclassificationmanager_classificationrunningstatus, fsrmpipeline/IFsrmClassificationManager2::ClassificationRunningStatus, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationRunningStatus, fsrmpipeline/IFsrmClassificationManager::ClassificationRunningStatus, fsrmpipeline/IFsrmClassificationManager::get_ClassificationRunningStatus, get_ClassificationRunningStatus
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
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
 - IFsrmClassificationManager::get_ClassificationRunningStatus
 - fsrmpipeline/IFsrmClassificationManager::get_ClassificationRunningStatus
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
 - IFsrmClassificationManager.ClassificationRunningStatus
 - IFsrmClassificationManager.get_ClassificationRunningStatus
 - IFsrmClassificationManager2.ClassificationRunningStatus
 - IFsrmClassificationManager2.get_ClassificationRunningStatus
 - FsrmClassificationManager.ClassificationRunningStatus
---

# IFsrmClassificationManager::get_ClassificationRunningStatus


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

The running status of the classification.

This property is read-only.

## -parameters

## -remarks

Used regardless of whether classification was scheduled (using the Task Scheduler) or run on demand (using 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">IFsrmClassificationManager::RunClassification</a>).

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationlasterror">IFsrmClassificationManager.ClassificationLastError</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">IFsrmClassificationManager::RunClassification</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-waitforclassificationcompletion">IFsrmClassificationManager::WaitForClassificationCompletion</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>