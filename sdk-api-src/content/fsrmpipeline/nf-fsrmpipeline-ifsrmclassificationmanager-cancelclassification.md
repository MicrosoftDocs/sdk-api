---
UID: NF:fsrmpipeline.IFsrmClassificationManager.CancelClassification
title: IFsrmClassificationManager::CancelClassification (fsrmpipeline.h)
description: Cancels classification if it is running.
helpviewer_keywords: ["CancelClassification","CancelClassification method [File Server Resource Manager]","CancelClassification method [File Server Resource Manager]","FsrmClassificationManager class","CancelClassification method [File Server Resource Manager]","IFsrmClassificationManager interface","CancelClassification method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","CancelClassification method","IFsrmClassificationManager interface [File Server Resource Manager]","CancelClassification method","IFsrmClassificationManager.CancelClassification","IFsrmClassificationManager2 interface [File Server Resource Manager]","CancelClassification method","IFsrmClassificationManager2::CancelClassification","IFsrmClassificationManager::CancelClassification","fs.ifsrmclassificationmanager_cancelclassification","fsrm.ifsrmclassificationmanager_cancelclassification","fsrmpipeline/IFsrmClassificationManager2::CancelClassification","fsrmpipeline/IFsrmClassificationManager::CancelClassification"]
old-location: fsrm\ifsrmclassificationmanager_cancelclassification.htm
tech.root: fsrm
ms.assetid: ff26acfd-71ff-49f4-a7ea-60825ff42f3b
ms.date: 12/05/2018
ms.keywords: CancelClassification, CancelClassification method [File Server Resource Manager], CancelClassification method [File Server Resource Manager],FsrmClassificationManager class, CancelClassification method [File Server Resource Manager],IFsrmClassificationManager interface, CancelClassification method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],CancelClassification method, IFsrmClassificationManager interface [File Server Resource Manager],CancelClassification method, IFsrmClassificationManager.CancelClassification, IFsrmClassificationManager2 interface [File Server Resource Manager],CancelClassification method, IFsrmClassificationManager2::CancelClassification, IFsrmClassificationManager::CancelClassification, fs.ifsrmclassificationmanager_cancelclassification, fsrm.ifsrmclassificationmanager_cancelclassification, fsrmpipeline/IFsrmClassificationManager2::CancelClassification, fsrmpipeline/IFsrmClassificationManager::CancelClassification
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
 - IFsrmClassificationManager::CancelClassification
 - fsrmpipeline/IFsrmClassificationManager::CancelClassification
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
 - IFsrmClassificationManager.CancelClassification
 - IFsrmClassificationManager2.CancelClassification
 - FsrmClassificationManager.CancelClassification
---

# IFsrmClassificationManager::CancelClassification


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Cancels classification if it is running.



## -returns

The method returns the following return values.

## -remarks

Cancels classification that was started manually using the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">IFsrmClassificationManager::RunClassification</a> 
    method or that was started on a schedule (see 
    <b>RunClassification</b> for details 
    on running classification on a schedule).

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
