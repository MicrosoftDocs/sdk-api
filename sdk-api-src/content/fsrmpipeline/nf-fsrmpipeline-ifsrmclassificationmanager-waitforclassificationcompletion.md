---
UID: NF:fsrmpipeline.IFsrmClassificationManager.WaitForClassificationCompletion
title: IFsrmClassificationManager::WaitForClassificationCompletion (fsrmpipeline.h)
description: Waits for the specified period of time or until classification has finished running.
helpviewer_keywords: ["FsrmClassificationManager class [File Server Resource Manager]","WaitForClassificationCompletion method","IFsrmClassificationManager interface [File Server Resource Manager]","WaitForClassificationCompletion method","IFsrmClassificationManager.WaitForClassificationCompletion","IFsrmClassificationManager2 interface [File Server Resource Manager]","WaitForClassificationCompletion method","IFsrmClassificationManager2::WaitForClassificationCompletion","IFsrmClassificationManager::WaitForClassificationCompletion","WaitForClassificationCompletion","WaitForClassificationCompletion method [File Server Resource Manager]","WaitForClassificationCompletion method [File Server Resource Manager]","FsrmClassificationManager class","WaitForClassificationCompletion method [File Server Resource Manager]","IFsrmClassificationManager interface","WaitForClassificationCompletion method [File Server Resource Manager]","IFsrmClassificationManager2 interface","fs.ifsrmclassificationmanager_waitforclassificationcompletion","fsrm.ifsrmclassificationmanager_waitforclassificationcompletion","fsrmpipeline/IFsrmClassificationManager2::WaitForClassificationCompletion","fsrmpipeline/IFsrmClassificationManager::WaitForClassificationCompletion"]
old-location: fsrm\ifsrmclassificationmanager_waitforclassificationcompletion.htm
tech.root: fsrm
ms.assetid: d288f84c-5078-40e3-ad32-6794f82157d5
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],WaitForClassificationCompletion method, IFsrmClassificationManager interface [File Server Resource Manager],WaitForClassificationCompletion method, IFsrmClassificationManager.WaitForClassificationCompletion, IFsrmClassificationManager2 interface [File Server Resource Manager],WaitForClassificationCompletion method, IFsrmClassificationManager2::WaitForClassificationCompletion, IFsrmClassificationManager::WaitForClassificationCompletion, WaitForClassificationCompletion, WaitForClassificationCompletion method [File Server Resource Manager], WaitForClassificationCompletion method [File Server Resource Manager],FsrmClassificationManager class, WaitForClassificationCompletion method [File Server Resource Manager],IFsrmClassificationManager interface, WaitForClassificationCompletion method [File Server Resource Manager],IFsrmClassificationManager2 interface, fs.ifsrmclassificationmanager_waitforclassificationcompletion, fsrm.ifsrmclassificationmanager_waitforclassificationcompletion, fsrmpipeline/IFsrmClassificationManager2::WaitForClassificationCompletion, fsrmpipeline/IFsrmClassificationManager::WaitForClassificationCompletion
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
 - IFsrmClassificationManager::WaitForClassificationCompletion
 - fsrmpipeline/IFsrmClassificationManager::WaitForClassificationCompletion
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
 - IFsrmClassificationManager.WaitForClassificationCompletion
 - IFsrmClassificationManager2.WaitForClassificationCompletion
 - FsrmClassificationManager.WaitForClassificationCompletion
---

# IFsrmClassificationManager::WaitForClassificationCompletion


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

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
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">IFsrmClassificationManager::RunClassification</a> 
    method.

After 
    <b>WaitForClassificationCompletion</b> 
    returns, access the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationlasterror">IFsrmClassificationManager.ClassificationLastError</a> 
    property to determine if the reports completed successfully.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationrunningstatus">IFsrmClassificationManager.ClassificationRunningStatus</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>