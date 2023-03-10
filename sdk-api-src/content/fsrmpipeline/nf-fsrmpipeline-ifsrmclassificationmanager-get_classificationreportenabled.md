---
UID: NF:fsrmpipeline.IFsrmClassificationManager.get_ClassificationReportEnabled
title: IFsrmClassificationManager::get_ClassificationReportEnabled (fsrmpipeline.h)
description: Determines whether classification reporting is enabled or not. (Get)
helpviewer_keywords: ["ClassificationReportEnabled property [File Server Resource Manager]","ClassificationReportEnabled property [File Server Resource Manager]","IFsrmClassificationManager interface","ClassificationReportEnabled property [File Server Resource Manager]","IFsrmClassificationManager2 interface","IFsrmClassificationManager interface [File Server Resource Manager]","ClassificationReportEnabled property","IFsrmClassificationManager.ClassificationReportEnabled","IFsrmClassificationManager.get_ClassificationReportEnabled","IFsrmClassificationManager2 interface [File Server Resource Manager]","ClassificationReportEnabled property","IFsrmClassificationManager2.ClassificationReportEnabled","IFsrmClassificationManager2::get_ClassificationReportEnabled","IFsrmClassificationManager2::put_ClassificationReportEnabled","IFsrmClassificationManager::ClassificationReportEnabled","IFsrmClassificationManager::get_ClassificationReportEnabled","IFsrmClassificationManager::put_ClassificationReportEnabled","fs.ifsrmclassificationmanager_classificationreportenabled","fsrm.ifsrmclassificationmanager_classificationreportenabled","fsrmpipeline/IFsrmClassificationManager2::ClassificationReportEnabled","fsrmpipeline/IFsrmClassificationManager2::get_ClassificationReportEnabled","fsrmpipeline/IFsrmClassificationManager2::put_ClassificationReportEnabled","fsrmpipeline/IFsrmClassificationManager::ClassificationReportEnabled","fsrmpipeline/IFsrmClassificationManager::get_ClassificationReportEnabled","fsrmpipeline/IFsrmClassificationManager::put_ClassificationReportEnabled","get_ClassificationReportEnabled"]
old-location: fsrm\ifsrmclassificationmanager_classificationreportenabled.htm
tech.root: fsrm
ms.assetid: a19a82fd-f00c-4663-b305-2cdc3bc863bd
ms.date: 12/05/2018
ms.keywords: ClassificationReportEnabled property [File Server Resource Manager], ClassificationReportEnabled property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationReportEnabled property [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationReportEnabled property, IFsrmClassificationManager.ClassificationReportEnabled, IFsrmClassificationManager.get_ClassificationReportEnabled, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationReportEnabled property, IFsrmClassificationManager2.ClassificationReportEnabled, IFsrmClassificationManager2::get_ClassificationReportEnabled, IFsrmClassificationManager2::put_ClassificationReportEnabled, IFsrmClassificationManager::ClassificationReportEnabled, IFsrmClassificationManager::get_ClassificationReportEnabled, IFsrmClassificationManager::put_ClassificationReportEnabled, fs.ifsrmclassificationmanager_classificationreportenabled, fsrm.ifsrmclassificationmanager_classificationreportenabled, fsrmpipeline/IFsrmClassificationManager2::ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager2::put_ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager::ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager::get_ClassificationReportEnabled, fsrmpipeline/IFsrmClassificationManager::put_ClassificationReportEnabled, get_ClassificationReportEnabled
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
 - IFsrmClassificationManager::get_ClassificationReportEnabled
 - fsrmpipeline/IFsrmClassificationManager::get_ClassificationReportEnabled
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
 - IFsrmClassificationManager.ClassificationReportEnabled
 - IFsrmClassificationManager.get_ClassificationReportEnabled
 - IFsrmClassificationManager.put_ClassificationReportEnabled
 - IFsrmClassificationManager2.ClassificationReportEnabled
 - IFsrmClassificationManager2.get_ClassificationReportEnabled
 - IFsrmClassificationManager2.put_ClassificationReportEnabled
---

# IFsrmClassificationManager::get_ClassificationReportEnabled


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Determines whether classification reporting is enabled or not.

This property is read/write.

## -parameters

## -remarks

Controls reporting regardless of whether classification was scheduled (using the Task Scheduler) or run on 
    demand (using 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">IFsrmClassificationManager::RunClassification</a>).

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationlastreportpathwithoutextension">IFsrmClassificationManager.ClassificationLastReportPathWithoutExtension</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationreportformats">IFsrmClassificationManager.ClassificationReportFormats</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationreportmailto">IFsrmClassificationManager.ClassificationReportMailTo</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
