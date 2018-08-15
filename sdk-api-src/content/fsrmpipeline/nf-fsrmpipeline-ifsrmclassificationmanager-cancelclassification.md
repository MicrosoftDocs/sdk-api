---
UID: NF:fsrmpipeline.IFsrmClassificationManager.CancelClassification
title: IFsrmClassificationManager::CancelClassification
author: windows-sdk-content
description: Cancels classification if it is running.
old-location: fsrm\ifsrmclassificationmanager_cancelclassification.htm
old-project: fsrm
ms.assetid: ff26acfd-71ff-49f4-a7ea-60825ff42f3b
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: CancelClassification, CancelClassification method [File Server Resource Manager], CancelClassification method [File Server Resource Manager],FsrmClassificationManager class, CancelClassification method [File Server Resource Manager],IFsrmClassificationManager interface, CancelClassification method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],CancelClassification method, IFsrmClassificationManager interface [File Server Resource Manager],CancelClassification method, IFsrmClassificationManager.CancelClassification, IFsrmClassificationManager2 interface [File Server Resource Manager],CancelClassification method, IFsrmClassificationManager2::CancelClassification, IFsrmClassificationManager::CancelClassification, fs.ifsrmclassificationmanager_cancelclassification, fsrm.ifsrmclassificationmanager_cancelclassification, fsrmpipeline/IFsrmClassificationManager2::CancelClassification, fsrmpipeline/IFsrmClassificationManager::CancelClassification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.redist: 
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
 - IFsrmClassificationManager.CancelClassification
 - IFsrmClassificationManager2.CancelClassification
 - FsrmClassificationManager.CancelClassification
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::CancelClassification


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Cancels classification if it is running.


## -parameters






## -returns



The method returns the following return values.




## -remarks



Cancels classification that was started manually using the 
    <a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a> 
    method or that was started on a schedule (see 
    <b>RunClassification</b> for details 
    on running classification on a schedule).




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

