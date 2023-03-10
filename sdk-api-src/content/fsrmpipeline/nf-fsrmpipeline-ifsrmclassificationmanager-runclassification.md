---
UID: NF:fsrmpipeline.IFsrmClassificationManager.RunClassification
title: IFsrmClassificationManager::RunClassification (fsrmpipeline.h)
description: Runs classification rules and generates the classification report.
helpviewer_keywords: ["FsrmClassificationManager class [File Server Resource Manager]","RunClassification method","IFsrmClassificationManager interface [File Server Resource Manager]","RunClassification method","IFsrmClassificationManager.RunClassification","IFsrmClassificationManager2 interface [File Server Resource Manager]","RunClassification method","IFsrmClassificationManager2::RunClassification","IFsrmClassificationManager::RunClassification","RunClassification","RunClassification method [File Server Resource Manager]","RunClassification method [File Server Resource Manager]","FsrmClassificationManager class","RunClassification method [File Server Resource Manager]","IFsrmClassificationManager interface","RunClassification method [File Server Resource Manager]","IFsrmClassificationManager2 interface","fs.ifsrmclassificationmanager_runclassification","fsrm.ifsrmclassificationmanager_runclassification","fsrmpipeline/IFsrmClassificationManager2::RunClassification","fsrmpipeline/IFsrmClassificationManager::RunClassification"]
old-location: fsrm\ifsrmclassificationmanager_runclassification.htm
tech.root: fsrm
ms.assetid: 50fdc5c8-d2eb-4206-b0fa-0de2696d29c7
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],RunClassification method, IFsrmClassificationManager interface [File Server Resource Manager],RunClassification method, IFsrmClassificationManager.RunClassification, IFsrmClassificationManager2 interface [File Server Resource Manager],RunClassification method, IFsrmClassificationManager2::RunClassification, IFsrmClassificationManager::RunClassification, RunClassification, RunClassification method [File Server Resource Manager], RunClassification method [File Server Resource Manager],FsrmClassificationManager class, RunClassification method [File Server Resource Manager],IFsrmClassificationManager interface, RunClassification method [File Server Resource Manager],IFsrmClassificationManager2 interface, fs.ifsrmclassificationmanager_runclassification, fsrm.ifsrmclassificationmanager_runclassification, fsrmpipeline/IFsrmClassificationManager2::RunClassification, fsrmpipeline/IFsrmClassificationManager::RunClassification
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
 - IFsrmClassificationManager::RunClassification
 - fsrmpipeline/IFsrmClassificationManager::RunClassification
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
 - IFsrmClassificationManager.RunClassification
 - IFsrmClassificationManager2.RunClassification
 - FsrmClassificationManager.RunClassification
---

# IFsrmClassificationManager::RunClassification


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Runs classification rules and generates the classification report.

## -parameters

### -param context [in]

Specifies the report subdirectory to which the classification report is written. For possible values, see 
      the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportgenerationcontext">FsrmReportGenerationContext</a> enumeration. 
      To set the report directory, call the 
      <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setoutputdirectory">IFsrmReportManager::SetOutputDirectory</a> 
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
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationrunningstatus">IFsrmClassificationManager.ClassificationRunningStatus</a> 
    property. To determine whether classification was successful, access the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationlasterror">ClassificationLastError</a> 
    property.

Classification generates the classification report only if reporting is enabled (see the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationreportenabled">IFsrmClassificationManager.ClassificationReportEnabled</a> 
    property).

To run classification on a schedule, use the Task Scheduler. Create a version 1.0 task. The command to run is 
    C:\Windows\System32\StorRept.exe. Specify "classification run" as the arguments to 
    StorRept.exe. StorRept.exe uses the 
    <b>FsrmReportGenerationContext_ScheduledReport</b> reporting context.

FSRM does not apply the classification rule if the rule, file, and cache are valid and have not changed.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>