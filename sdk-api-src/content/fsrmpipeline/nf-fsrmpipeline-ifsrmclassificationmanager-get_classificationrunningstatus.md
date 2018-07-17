---
UID: NF:fsrmpipeline.IFsrmClassificationManager.get_ClassificationRunningStatus
title: IFsrmClassificationManager::get_ClassificationRunningStatus
author: windows-sdk-content
description: The running status of the classification.
old-location: fsrm\ifsrmclassificationmanager_classificationrunningstatus.htm
old-project: Fsrm
ms.assetid: f0a10671-9383-4935-b773-31f047732e27
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ClassificationRunningStatus property [File Server Resource Manager], ClassificationRunningStatus property [File Server Resource Manager],FsrmClassificationManager class, ClassificationRunningStatus property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationRunningStatus property [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassificationRunningStatus property, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationRunningStatus property, IFsrmClassificationManager.ClassificationRunningStatus, IFsrmClassificationManager.get_ClassificationRunningStatus, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationRunningStatus property, IFsrmClassificationManager2.ClassificationRunningStatus, IFsrmClassificationManager2::get_ClassificationRunningStatus, IFsrmClassificationManager::ClassificationRunningStatus, IFsrmClassificationManager::get_ClassificationRunningStatus, fs.ifsrmclassificationmanager_classificationrunningstatus, fsrm.ifsrmclassificationmanager_classificationrunningstatus, fsrmpipeline/IFsrmClassificationManager2::ClassificationRunningStatus, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationRunningStatus, fsrmpipeline/IFsrmClassificationManager::ClassificationRunningStatus, fsrmpipeline/IFsrmClassificationManager::get_ClassificationRunningStatus, get_ClassificationRunningStatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::get_ClassificationRunningStatus


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

The running status of the classification.

This property is read-only.


## -parameters


## -remarks



Used regardless of whether classification was scheduled (using the Task Scheduler) or run on demand (using 
    <a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a>).




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/02c62b7d-a128-432a-a15a-51de092b5bab">IFsrmClassificationManager.ClassificationLastError</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a>



<a href="https://msdn.microsoft.com/d288f84c-5078-40e3-ad32-6794f82157d5">IFsrmClassificationManager::WaitForClassificationCompletion</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

