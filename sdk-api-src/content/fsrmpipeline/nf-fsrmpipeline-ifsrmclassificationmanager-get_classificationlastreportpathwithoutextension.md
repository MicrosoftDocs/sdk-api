---
UID: NF:fsrmpipeline.IFsrmClassificationManager.get_ClassificationLastReportPathWithoutExtension
title: IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension (fsrmpipeline.h)
description: The local directory path where the reports were stored the last time that classification ran.
helpviewer_keywords: ["ClassificationLastReportPathWithoutExtension property [File Server Resource Manager]","ClassificationLastReportPathWithoutExtension property [File Server Resource Manager]","IFsrmClassificationManager interface","ClassificationLastReportPathWithoutExtension property [File Server Resource Manager]","IFsrmClassificationManager2 interface","IFsrmClassificationManager interface [File Server Resource Manager]","ClassificationLastReportPathWithoutExtension property","IFsrmClassificationManager.ClassificationLastReportPathWithoutExtension","IFsrmClassificationManager.get_ClassificationLastReportPathWithoutExtension","IFsrmClassificationManager2 interface [File Server Resource Manager]","ClassificationLastReportPathWithoutExtension property","IFsrmClassificationManager2.ClassificationLastReportPathWithoutExtension","IFsrmClassificationManager2::get_ClassificationLastReportPathWithoutExtension","IFsrmClassificationManager::ClassificationLastReportPathWithoutExtension","IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension","fs.ifsrmclassificationmanager_classificationlastreportpathwithoutextension","fsrm.ifsrmclassificationmanager_classificationlastreportpathwithoutextension","fsrmpipeline/IFsrmClassificationManager2::ClassificationLastReportPathWithoutExtension","fsrmpipeline/IFsrmClassificationManager2::get_ClassificationLastReportPathWithoutExtension","fsrmpipeline/IFsrmClassificationManager::ClassificationLastReportPathWithoutExtension","fsrmpipeline/IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension","get_ClassificationLastReportPathWithoutExtension"]
old-location: fsrm\ifsrmclassificationmanager_classificationlastreportpathwithoutextension.htm
tech.root: fsrm
ms.assetid: bdc32bbc-e8e5-48ed-97a1-0b42db3c3676
ms.date: 12/05/2018
ms.keywords: ClassificationLastReportPathWithoutExtension property [File Server Resource Manager], ClassificationLastReportPathWithoutExtension property [File Server Resource Manager],IFsrmClassificationManager interface, ClassificationLastReportPathWithoutExtension property [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],ClassificationLastReportPathWithoutExtension property, IFsrmClassificationManager.ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager.get_ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassificationLastReportPathWithoutExtension property, IFsrmClassificationManager2.ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager2::get_ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager::ClassificationLastReportPathWithoutExtension, IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension, fs.ifsrmclassificationmanager_classificationlastreportpathwithoutextension, fsrm.ifsrmclassificationmanager_classificationlastreportpathwithoutextension, fsrmpipeline/IFsrmClassificationManager2::ClassificationLastReportPathWithoutExtension, fsrmpipeline/IFsrmClassificationManager2::get_ClassificationLastReportPathWithoutExtension, fsrmpipeline/IFsrmClassificationManager::ClassificationLastReportPathWithoutExtension, fsrmpipeline/IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension, get_ClassificationLastReportPathWithoutExtension
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
 - IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension
 - fsrmpipeline/IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension
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
 - IFsrmClassificationManager.ClassificationLastReportPathWithoutExtension
 - IFsrmClassificationManager.get_ClassificationLastReportPathWithoutExtension
 - IFsrmClassificationManager2.ClassificationLastReportPathWithoutExtension
 - IFsrmClassificationManager2.get_ClassificationLastReportPathWithoutExtension
---

# IFsrmClassificationManager::get_ClassificationLastReportPathWithoutExtension


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

The local directory path where the reports were stored the last time that classification 
    ran.

This property is read-only.

## -parameters

## -remarks

If the reports failed, this is the path where the reports would have been stored. The directory may contain 
    reports that completed successfully before the failure occurred. The value passed to 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setoutputdirectory">IFsrmReportManager::SetOutputDirectory</a>, 
    if any, and the reporting context determine the path.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationreportenabled">IFsrmClassificationManager.ClassificationReportEnabled</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setoutputdirectory">IFsrmReportManager::SetOutputDirectory</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>