---
UID: NF:fsrmpipeline.IFsrmClassificationManager.get_ClassificationLastError
title: IFsrmClassificationManager::get_ClassificationLastError (fsrmpipeline.h)
author: windows-sdk-content
description: The error message from the last time that classification was run.
old-location: fsrm\ifsrmclassificationmanager_classificationlasterror.htm
tech.root: fsrm
ms.assetid: 02c62b7d-a128-432a-a15a-51de092b5bab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClassificationLastError property [File Server Resource Manager], ClassificationLastError property [File Server Resource Manager],FsrmClassificationManager class, ClassificationLastError property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationLastError property [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassificationLastError property, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationLastError property, IFsrmClassificationManager.ClassificationLastError, IFsrmClassificationManager.get_ClassificationLastError, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationLastError property, IFsrmClassificationManager2.ClassificationLastError, IFsrmClassificationManager2::get_ClassificationLastError, IFsrmClassificationManager::ClassificationLastError, IFsrmClassificationManager::get_ClassificationLastError, fs.ifsrmclassificationmanager_classificationlasterror, fsrm.ifsrmclassificationmanager_classificationlasterror, fsrmpipeline/IFsrmClassificationManager2::ClassificationLastError, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationLastError, fsrmpipeline/IFsrmClassificationManager::ClassificationLastError, fsrmpipeline/IFsrmClassificationManager::get_ClassificationLastError, get_ClassificationLastError
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmClassificationManager.ClassificationLastError
 - IFsrmClassificationManager.get_ClassificationLastError
 - IFsrmClassificationManager2.ClassificationLastError
 - IFsrmClassificationManager2.get_ClassificationLastError
 - FsrmClassificationManager.ClassificationLastError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmClassificationManager::get_ClassificationLastError


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

The error message from the last time that classification was run.

This property is read-only.


## -parameters


## -remarks



The property is set after classification is run either manually using 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">IFsrmClassificationManager::RunClassification</a> 
    or is scheduled using Task Scheduler.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationrunningstatus">IFsrmClassificationManager.ClassificationRunningStatus</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
 

 

