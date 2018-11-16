---
UID: NF:fsrmpipeline.IFsrmClassificationManager.put_ClassificationReportMailTo
title: IFsrmClassificationManager::put_ClassificationReportMailTo
author: windows-sdk-content
description: The email address to which to send the classification reports, if any.
old-location: fsrm\ifsrmclassificationmanager_classificationreportmailto.htm
tech.root: Fsrm
ms.assetid: fa998edc-7ef8-43fa-a83a-7e4ba911e970
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ClassificationReportMailTo property [File Server Resource Manager], ClassificationReportMailTo property [File Server Resource Manager],FsrmClassificationManager class, ClassificationReportMailTo property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationReportMailTo property [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassificationReportMailTo property, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationReportMailTo property, IFsrmClassificationManager.ClassificationReportMailTo, IFsrmClassificationManager.put_ClassificationReportMailTo, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationReportMailTo property, IFsrmClassificationManager2.ClassificationReportMailTo, IFsrmClassificationManager2::get_ClassificationReportMailTo, IFsrmClassificationManager2::put_ClassificationReportMailTo, IFsrmClassificationManager::ClassificationReportMailTo, IFsrmClassificationManager::get_ClassificationReportMailTo, IFsrmClassificationManager::put_ClassificationReportMailTo, fs.ifsrmclassificationmanager_classificationreportmailto, fsrm.ifsrmclassificationmanager_classificationreportmailto, fsrmpipeline/IFsrmClassificationManager2::ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager2::put_ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager::ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager::get_ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager::put_ClassificationReportMailTo, put_ClassificationReportMailTo
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
 - IFsrmClassificationManager.ClassificationReportMailTo
 - IFsrmClassificationManager.get_ClassificationReportMailTo
 - IFsrmClassificationManager.put_ClassificationReportMailTo
 - IFsrmClassificationManager2.ClassificationReportMailTo
 - IFsrmClassificationManager2.get_ClassificationReportMailTo
 - IFsrmClassificationManager2.put_ClassificationReportMailTo
 - FsrmClassificationManager.ClassificationReportMailTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmpipeline.h
: 
- IFsrmClassificationManager.put_ClassificationReportMailTo
: 
---

# IFsrmClassificationManager::put_ClassificationReportMailTo


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

The email address to which to send the classification reports, if any.

This property is read/write.


## -parameters


## -remarks



This property is optional.

The email message is sent only if the classification finishes successfully. Email is not sent for 
    <b>FsrmReportType_ExportReport</b> report types. The reports are attached to the email 
    message. You can specify [Admin Email] to send notification to the administrator (if the 
    <a href="https://msdn.microsoft.com/5985f697-f982-481c-896e-e6c3834f645d">IFsrmSetting::AdminEmail</a> property is set). The 
    subject is "&lt;ReportType&gt;: &lt;ReportName&gt;". The body of the email message is empty.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

