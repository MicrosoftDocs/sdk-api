---
UID: NF:fsrmpipeline.IFsrmClassificationManager.put_ClassificationReportEnabled
title: IFsrmClassificationManager::put_ClassificationReportEnabled
author: windows-driver-content
description: Determines whether classification reporting is enabled or not.
old-location: fsrm\ifsrmclassificationmanager_classificationreportenabled.htm
old-project: Fsrm
ms.assetid: a19a82fd-f00c-4663-b305-2cdc3bc863bd
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: ClassificationReportEnabled property [File Server Resource Manager], ClassificationReportEnabled property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationReportEnabled property [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationReportEnabled property, IFsrmClassificationManager.ClassificationReportEnabled, IFsrmClassificationManager.put_ClassificationReportEnabled, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationReportEnabled property, IFsrmClassificationManager2.ClassificationReportEnabled, IFsrmClassificationManager2::get_ClassificationReportEnabled, IFsrmClassificationManager2::put_ClassificationReportEnabled, IFsrmClassificationManager::ClassificationReportEnabled, IFsrmClassificationManager::get_ClassificationReportEnabled, IFsrmClassificationManager::put_ClassificationReportEnabled, fs.ifsrmclassificationmanager_classificationreportenabled, fsrm.ifsrmclassificationmanager_classificationreportenabled, fsrmpipeline/IFsrmClassificationManager2::ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager2::put_ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager::ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager::get_ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager::put_ClassificationReportEnabled, put_ClassificationReportEnabled
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmClassificationManager.ClassificationReportEnabled
-	IFsrmClassificationManager.get_ClassificationReportEnabled
-	IFsrmClassificationManager.put_ClassificationReportEnabled
-	IFsrmClassificationManager2.ClassificationReportEnabled
-	IFsrmClassificationManager2.get_ClassificationReportEnabled
-	IFsrmClassificationManager2.put_ClassificationReportEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::put_ClassificationReportEnabled


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Determines whether classification reporting is enabled or not.

This property is read/write.


## -parameters


## -remarks



Controls reporting regardless of whether classification was scheduled (using the Task Scheduler) or run on 
    demand (using 
    <a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a>).




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/bdc32bbc-e8e5-48ed-97a1-0b42db3c3676">IFsrmClassificationManager.ClassificationLastReportPathWithoutExtension</a>



<a href="https://msdn.microsoft.com/a9402faa-06f9-4cfe-9a36-a2fc1a581824">IFsrmClassificationManager.ClassificationReportFormats</a>



<a href="https://msdn.microsoft.com/fa998edc-7ef8-43fa-a83a-7e4ba911e970">IFsrmClassificationManager.ClassificationReportMailTo</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

