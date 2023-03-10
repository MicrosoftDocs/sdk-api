---
UID: NF:fsrmpipeline.IFsrmClassificationManager.put_ClassificationReportMailTo
title: IFsrmClassificationManager::put_ClassificationReportMailTo (fsrmpipeline.h)
description: The email address to which to send the classification reports, if any. (Put)
helpviewer_keywords: ["ClassificationReportMailTo property [File Server Resource Manager]","ClassificationReportMailTo property [File Server Resource Manager]","FsrmClassificationManager class","ClassificationReportMailTo property [File Server Resource Manager]","IFsrmClassificationManager interface","ClassificationReportMailTo property [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","ClassificationReportMailTo property","IFsrmClassificationManager interface [File Server Resource Manager]","ClassificationReportMailTo property","IFsrmClassificationManager.ClassificationReportMailTo","IFsrmClassificationManager.put_ClassificationReportMailTo","IFsrmClassificationManager2 interface [File Server Resource Manager]","ClassificationReportMailTo property","IFsrmClassificationManager2.ClassificationReportMailTo","IFsrmClassificationManager2::get_ClassificationReportMailTo","IFsrmClassificationManager2::put_ClassificationReportMailTo","IFsrmClassificationManager::ClassificationReportMailTo","IFsrmClassificationManager::get_ClassificationReportMailTo","IFsrmClassificationManager::put_ClassificationReportMailTo","fs.ifsrmclassificationmanager_classificationreportmailto","fsrm.ifsrmclassificationmanager_classificationreportmailto","fsrmpipeline/IFsrmClassificationManager2::ClassificationReportMailTo","fsrmpipeline/IFsrmClassificationManager2::get_ClassificationReportMailTo","fsrmpipeline/IFsrmClassificationManager2::put_ClassificationReportMailTo","fsrmpipeline/IFsrmClassificationManager::ClassificationReportMailTo","fsrmpipeline/IFsrmClassificationManager::get_ClassificationReportMailTo","fsrmpipeline/IFsrmClassificationManager::put_ClassificationReportMailTo","put_ClassificationReportMailTo"]
old-location: fsrm\ifsrmclassificationmanager_classificationreportmailto.htm
tech.root: fsrm
ms.assetid: fa998edc-7ef8-43fa-a83a-7e4ba911e970
ms.date: 12/05/2018
ms.keywords: ClassificationReportMailTo property [File Server Resource Manager], ClassificationReportMailTo property [File Server Resource Manager],FsrmClassificationManager class, ClassificationReportMailTo property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationReportMailTo property [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassificationReportMailTo property, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationReportMailTo property, IFsrmClassificationManager.ClassificationReportMailTo, IFsrmClassificationManager.put_ClassificationReportMailTo, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationReportMailTo property, IFsrmClassificationManager2.ClassificationReportMailTo, IFsrmClassificationManager2::get_ClassificationReportMailTo, IFsrmClassificationManager2::put_ClassificationReportMailTo, IFsrmClassificationManager::ClassificationReportMailTo, IFsrmClassificationManager::get_ClassificationReportMailTo, IFsrmClassificationManager::put_ClassificationReportMailTo, fs.ifsrmclassificationmanager_classificationreportmailto, fsrm.ifsrmclassificationmanager_classificationreportmailto, fsrmpipeline/IFsrmClassificationManager2::ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager2::put_ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager::ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager::get_ClassificationReportMailTo, fsrmpipeline/IFsrmClassificationManager::put_ClassificationReportMailTo, put_ClassificationReportMailTo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmClassificationManager::put_ClassificationReportMailTo
 - fsrmpipeline/IFsrmClassificationManager::put_ClassificationReportMailTo
dev_langs:
 - c++
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
---

# IFsrmClassificationManager::put_ClassificationReportMailTo


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

The email address to which to send the classification reports, if any.

This property is read/write.

## -parameters

## -remarks

This property is optional.

The email message is sent only if the classification finishes successfully. Email is not sent for 
    <b>FsrmReportType_ExportReport</b> report types. The reports are attached to the email 
    message. You can specify [Admin Email] to send notification to the administrator (if the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_adminemail">IFsrmSetting::AdminEmail</a> property is set). The 
    subject is "&lt;ReportType&gt;: &lt;ReportName&gt;". The body of the email message is empty.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
