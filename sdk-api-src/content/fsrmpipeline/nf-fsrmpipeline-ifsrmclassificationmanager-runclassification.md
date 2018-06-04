---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

