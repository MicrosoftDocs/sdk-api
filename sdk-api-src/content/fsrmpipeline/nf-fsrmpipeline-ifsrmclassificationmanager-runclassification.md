---
UID: NF:fsrmpipeline.IFsrmClassificationManager.RunClassification
title: IFsrmClassificationManager::RunClassification (fsrmpipeline.h)
author: windows-sdk-content
description: Runs classification rules and generates the classification report.
old-location: fsrm\ifsrmclassificationmanager_runclassification.htm
tech.root: fsrm
ms.assetid: 50fdc5c8-d2eb-4206-b0fa-0de2696d29c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],RunClassification method, IFsrmClassificationManager interface [File Server Resource Manager],RunClassification method, IFsrmClassificationManager.RunClassification, IFsrmClassificationManager2 interface [File Server Resource Manager],RunClassification method, IFsrmClassificationManager2::RunClassification, IFsrmClassificationManager::RunClassification, RunClassification, RunClassification method [File Server Resource Manager], RunClassification method [File Server Resource Manager],FsrmClassificationManager class, RunClassification method [File Server Resource Manager],IFsrmClassificationManager interface, RunClassification method [File Server Resource Manager],IFsrmClassificationManager2 interface, fs.ifsrmclassificationmanager_runclassification, fsrm.ifsrmclassificationmanager_runclassification, fsrmpipeline/IFsrmClassificationManager2::RunClassification, fsrmpipeline/IFsrmClassificationManager::RunClassification
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
 - IFsrmClassificationManager.RunClassification
 - IFsrmClassificationManager2.RunClassification
 - FsrmClassificationManager.RunClassification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmClassificationManager::RunClassification


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Runs classification rules and generates the classification report.


## -parameters




### -param context [in]

Specifies the report subdirectory to which the classification report is written. For possible values, see 
      the <a href="https://msdn.microsoft.com/02e18cc2-7c5e-473f-8a7f-e310bfb1c57d">FsrmReportGenerationContext</a> enumeration. 
      To set the report directory, call the 
      <a href="https://msdn.microsoft.com/5bbc4255-1fed-45c5-bb13-41ee7c47ed56">IFsrmReportManager::SetOutputDirectory</a> 
      method.


### -param reserved [in]

Must be <b>NULL</b>.


## -returns



The method returns the following return values.




## -remarks



To run classification, there must be at least one property defined, at least one rule that references one of 
    the defined properties, and a registered classification module.

If you call this method and the classification is already queued or running, the method returns an error. To 
    determine whether classification is running, access the 
    <a href="https://msdn.microsoft.com/f0a10671-9383-4935-b773-31f047732e27">IFsrmClassificationManager.ClassificationRunningStatus</a> 
    property. To determine whether classification was successful, access the 
    <a href="https://msdn.microsoft.com/02c62b7d-a128-432a-a15a-51de092b5bab">ClassificationLastError</a> 
    property.

Classification generates the classification report only if reporting is enabled (see the 
    <a href="https://msdn.microsoft.com/a19a82fd-f00c-4663-b305-2cdc3bc863bd">IFsrmClassificationManager.ClassificationReportEnabled</a> 
    property).

To run classification on a schedule, use the Task Scheduler. Create a version 1.0 task. The command to run is 
    C:\Windows\System32\StorRept.exe. Specify "classification run" as the arguments to 
    StorRept.exe. StorRept.exe uses the 
    <b>FsrmReportGenerationContext_ScheduledReport</b> reporting context.

FSRM does not apply the classification rule if the rule, file, and cache are valid and have not changed.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

