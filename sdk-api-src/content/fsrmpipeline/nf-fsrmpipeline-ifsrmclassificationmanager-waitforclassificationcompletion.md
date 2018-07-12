---
UID: NF:fsrmpipeline.IFsrmClassificationManager.WaitForClassificationCompletion
title: IFsrmClassificationManager::WaitForClassificationCompletion
author: windows-sdk-content
description: Waits for the specified period of time or until classification has finished running.
old-location: fsrm\ifsrmclassificationmanager_waitforclassificationcompletion.htm
old-project: fsrm
ms.assetid: d288f84c-5078-40e3-ad32-6794f82157d5
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],WaitForClassificationCompletion method, IFsrmClassificationManager interface [File Server Resource Manager],WaitForClassificationCompletion method, IFsrmClassificationManager.WaitForClassificationCompletion, IFsrmClassificationManager2 interface [File Server Resource Manager],WaitForClassificationCompletion method, IFsrmClassificationManager2::WaitForClassificationCompletion, IFsrmClassificationManager::WaitForClassificationCompletion, WaitForClassificationCompletion, WaitForClassificationCompletion method [File Server Resource Manager], WaitForClassificationCompletion method [File Server Resource Manager],FsrmClassificationManager class, WaitForClassificationCompletion method [File Server Resource Manager],IFsrmClassificationManager interface, WaitForClassificationCompletion method [File Server Resource Manager],IFsrmClassificationManager2 interface, fs.ifsrmclassificationmanager_waitforclassificationcompletion, fsrm.ifsrmclassificationmanager_waitforclassificationcompletion, fsrmpipeline/IFsrmClassificationManager2::WaitForClassificationCompletion, fsrmpipeline/IFsrmClassificationManager::WaitForClassificationCompletion
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
 - IFsrmClassificationManager.WaitForClassificationCompletion
 - IFsrmClassificationManager2.WaitForClassificationCompletion
 - FsrmClassificationManager.WaitForClassificationCompletion
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::WaitForClassificationCompletion


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Waits for the specified period of time or until classification has finished running.


## -parameters




### -param waitSeconds [in]

The number of seconds to wait for classification and the reports to complete. The method returns when the 
      period expires or classification and the reports complete. To wait indefinitely, set the value to 
      –1. The value must be in the range from  –1 through 2,147,483.


### -param completed [out]

Is <b>VARIANT_TRUE</b> if the reports completed; otherwise, 
      <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -remarks



To run the classification, call the 
    <a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a> 
    method.

After 
    <b>WaitForClassificationCompletion</b> 
    returns, access the 
    <a href="https://msdn.microsoft.com/02c62b7d-a128-432a-a15a-51de092b5bab">IFsrmClassificationManager.ClassificationLastError</a> 
    property to determine if the reports completed successfully.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/f0a10671-9383-4935-b773-31f047732e27">IFsrmClassificationManager.ClassificationRunningStatus</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

