---
UID: NF:fsrmpipeline.IFsrmClassificationManager.get_ClassificationLastError
title: IFsrmClassificationManager::get_ClassificationLastError
author: windows-sdk-content
description: The error message from the last time that classification was run.
old-location: fsrm\ifsrmclassificationmanager_classificationlasterror.htm
tech.root: Fsrm
ms.assetid: 02c62b7d-a128-432a-a15a-51de092b5bab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClassificationLastError property [File Server Resource Manager], ClassificationLastError property [File Server Resource Manager],FsrmClassificationManager class, ClassificationLastError property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationLastError property [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassificationLastError property, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationLastError property, IFsrmClassificationManager.ClassificationLastError, IFsrmClassificationManager.get_ClassificationLastError, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationLastError property, IFsrmClassificationManager2.ClassificationLastError, IFsrmClassificationManager2::get_ClassificationLastError, IFsrmClassificationManager::ClassificationLastError, IFsrmClassificationManager::get_ClassificationLastError, fs.ifsrmclassificationmanager_classificationlasterror, fsrm.ifsrmclassificationmanager_classificationlasterror, fsrmpipeline/IFsrmClassificationManager2::ClassificationLastError, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationLastError, fsrmpipeline/IFsrmClassificationManager::ClassificationLastError, fsrmpipeline/IFsrmClassificationManager::get_ClassificationLastError, get_ClassificationLastError
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IFsrmClassificationManager::get_ClassificationLastError


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

The error message from the last time that classification was run.

This property is read-only.


## -parameters


## -remarks



The property is set after classification is run either manually using 
    <a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a> 
    or is scheduled using Task Scheduler.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/f0a10671-9383-4935-b773-31f047732e27">IFsrmClassificationManager.ClassificationRunningStatus</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

