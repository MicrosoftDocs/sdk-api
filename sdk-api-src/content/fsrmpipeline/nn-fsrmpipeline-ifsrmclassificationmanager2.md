---
UID: NN:fsrmpipeline.IFsrmClassificationManager2
title: IFsrmClassificationManager2 (fsrmpipeline.h)
description: Manages file classification. Use this interface to define properties to use in classification, add classification rules for classifying files, define classification and storage modules, and enable classification reporting. (IFsrmClassificationManager2)
helpviewer_keywords: ["IFsrmClassificationManager2","IFsrmClassificationManager2 interface [File Server Resource Manager]","IFsrmClassificationManager2 interface [File Server Resource Manager]","described","fs.ifsrmclassificationmanager2","fsrm.ifsrmclassificationmanager2","fsrmpipeline/IFsrmClassificationManager2"]
old-location: fsrm\ifsrmclassificationmanager2.htm
tech.root: fsrm
ms.assetid: 6ff821e3-f0bd-4c66-8ced-edbbfbc8503b
ms.date: 12/05/2018
ms.keywords: IFsrmClassificationManager2, IFsrmClassificationManager2 interface [File Server Resource Manager], IFsrmClassificationManager2 interface [File Server Resource Manager],described, fs.ifsrmclassificationmanager2, fsrm.ifsrmclassificationmanager2, fsrmpipeline/IFsrmClassificationManager2
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmPipeline.idl
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
 - IFsrmClassificationManager2
 - fsrmpipeline/IFsrmClassificationManager2
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
 - IFsrmClassificationManager2
---

# IFsrmClassificationManager2 interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Manages file classification. Use this interface to define properties to use in classification, add 
    classification rules for classifying files, define classification and storage modules, and enable classification 
    reporting.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmClassificationManager</b> as the class identifier and 
    <code>__uuidof(IFsrmClassificationManager2)</code> as the interface 
    identifier or use the use the "Fsrm.FsrmClassificationManager" program identifier.

## -inheritance

The <b>IFsrmClassificationManager2</b> interface inherits from <b>IFsrmClassificationManager</b>. <b>IFsrmClassificationManager2</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
