---
UID: NF:fsrmpipeline.IFsrmClassificationManager.get_ClassificationLastReportPathWithoutExtension
title: IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension method
author: windows-driver-content
description: The local directory path where the reports were stored the last time that classification ran.
old-location: fsrm\ifsrmclassificationmanager_classificationlastreportpathwithoutextension.htm
old-project: Fsrm
ms.assetid: bdc32bbc-e8e5-48ed-97a1-0b42db3c3676
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ClassificationLastReportPathWithoutExtension property [File Server Resource Manager], ClassificationLastReportPathWithoutExtension property [File Server Resource Manager], IFsrmClassificationManager interface, ClassificationLastReportPathWithoutExtension property [File Server Resource Manager], IFsrmClassificationManager2 interface, IFsrmClassificationManager, IFsrmClassificationManager interface [File Server Resource Manager], ClassificationLastReportPathWithoutExtension property, IFsrmClassificationManager.ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager2 interface [File Server Resource Manager], ClassificationLastReportPathWithoutExtension property, IFsrmClassificationManager2.ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager2::get_ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension, fs.ifsrmclassificationmanager_classificationlastreportpathwithoutextension, fsrm.ifsrmclassificationmanager_classificationlastreportpathwithoutextension, fsrmpipeline/IFsrmClassificationManager2::ClassificationLastReportPathWithoutExtension, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationLastReportPathWithoutExtension, fsrmpipeline/IFsrmClassificationManager::ClassificationLastReportPathWithoutExtension, fsrmpipeline/IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension, get_ClassificationLastReportPathWithoutExtension,IFsrmClassificationManager.get_ClassificationLastReportPathWithoutExtension
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
-	IFsrmClassificationManager.ClassificationLastReportPathWithoutExtension
-	IFsrmClassificationManager.get_ClassificationLastReportPathWithoutExtension
-	IFsrmClassificationManager2.ClassificationLastReportPathWithoutExtension
-	IFsrmClassificationManager2.get_ClassificationLastReportPathWithoutExtension
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension method


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

The local directory path where the reports were stored the last time that classification 
    ran.

This property is read-only.


## -parameters


## -remarks



If the reports failed, this is the path where the reports would have been stored. The directory may contain 
    reports that completed successfully before the failure occurred. The value passed to 
    <a href="https://msdn.microsoft.com/5bbc4255-1fed-45c5-bb13-41ee7c47ed56">IFsrmReportManager::SetOutputDirectory</a>, 
    if any, and the reporting context determine the path.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/a19a82fd-f00c-4663-b305-2cdc3bc863bd">IFsrmClassificationManager.ClassificationReportEnabled</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/5bbc4255-1fed-45c5-bb13-41ee7c47ed56">IFsrmReportManager::SetOutputDirectory</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

