---
UID: NF:fsrmpipeline.IFsrmClassificationManager.put_Logging
title: IFsrmClassificationManager::put_Logging (fsrmpipeline.h)
description: The types of logging to perform when running the classification rules. (Put)
helpviewer_keywords: ["FsrmClassificationManager class [File Server Resource Manager]","Logging property","IFsrmClassificationManager interface [File Server Resource Manager]","Logging property","IFsrmClassificationManager.Logging","IFsrmClassificationManager.put_Logging","IFsrmClassificationManager2 interface [File Server Resource Manager]","Logging property","IFsrmClassificationManager2.Logging","IFsrmClassificationManager2::get_Logging","IFsrmClassificationManager2::put_Logging","IFsrmClassificationManager::Logging","IFsrmClassificationManager::get_Logging","IFsrmClassificationManager::put_Logging","Logging property [File Server Resource Manager]","Logging property [File Server Resource Manager]","FsrmClassificationManager class","Logging property [File Server Resource Manager]","IFsrmClassificationManager interface","Logging property [File Server Resource Manager]","IFsrmClassificationManager2 interface","fs.ifsrmclassificationmanager_logging","fsrm.ifsrmclassificationmanager_logging","fsrmpipeline/IFsrmClassificationManager2::Logging","fsrmpipeline/IFsrmClassificationManager2::get_Logging","fsrmpipeline/IFsrmClassificationManager2::put_Logging","fsrmpipeline/IFsrmClassificationManager::Logging","fsrmpipeline/IFsrmClassificationManager::get_Logging","fsrmpipeline/IFsrmClassificationManager::put_Logging","put_Logging"]
old-location: fsrm\ifsrmclassificationmanager_logging.htm
tech.root: fsrm
ms.assetid: c22f646b-36dc-45b8-a9ad-81ce6adab5bf
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],Logging property, IFsrmClassificationManager interface [File Server Resource Manager],Logging property, IFsrmClassificationManager.Logging, IFsrmClassificationManager.put_Logging, IFsrmClassificationManager2 interface [File Server Resource Manager],Logging property, IFsrmClassificationManager2.Logging, IFsrmClassificationManager2::get_Logging, IFsrmClassificationManager2::put_Logging, IFsrmClassificationManager::Logging, IFsrmClassificationManager::get_Logging, IFsrmClassificationManager::put_Logging, Logging property [File Server Resource Manager], Logging property [File Server Resource Manager],FsrmClassificationManager class, Logging property [File Server Resource Manager],IFsrmClassificationManager interface, Logging property [File Server Resource Manager],IFsrmClassificationManager2 interface, fs.ifsrmclassificationmanager_logging, fsrm.ifsrmclassificationmanager_logging, fsrmpipeline/IFsrmClassificationManager2::Logging, fsrmpipeline/IFsrmClassificationManager2::get_Logging, fsrmpipeline/IFsrmClassificationManager2::put_Logging, fsrmpipeline/IFsrmClassificationManager::Logging, fsrmpipeline/IFsrmClassificationManager::get_Logging, fsrmpipeline/IFsrmClassificationManager::put_Logging, put_Logging
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
 - IFsrmClassificationManager::put_Logging
 - fsrmpipeline/IFsrmClassificationManager::put_Logging
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
 - IFsrmClassificationManager.Logging
 - IFsrmClassificationManager.get_Logging
 - IFsrmClassificationManager.put_Logging
 - IFsrmClassificationManager2.Logging
 - IFsrmClassificationManager2.get_Logging
 - IFsrmClassificationManager2.put_Logging
 - FsrmClassificationManager.Logging
---

# IFsrmClassificationManager::put_Logging


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

The types of logging to perform when running the classification rules.

This property is read/write.

## -parameters

## -remarks

The log file for the <b>FsrmClassificationLoggingFlags_ClassificationsInLogFile</b> and 
    <b>FsrmClassificationLoggingFlags_ErrorsInLogFile</b> logging options are stored in the 
    reports directory. The name of the 
    <b>FsrmClassificationLoggingFlags_ClassificationsInLogFile</b> log file is 
    "<i>ClassifierName</i>-<i>FsrmServerName(FQDN)</i>-<i>TimeStamp</i>.xml". 
    The log file contains one entry per property assignment to a specific file. Each log entry specifies the:

<ul>
<li>File name (full path)</li>
<li>Property</li>
<li>Value assigned</li>
<li>Rule applied</li>
<li>Result (whether the classification succeeded)</li>
</ul>
The name of the <b>FsrmClassificationLoggingFlags_ErrorsInLogFile</b> log file is 
    "<i>ClassifierName</i><i>Errors</i>-<i>FQDNServerName</i>-<i>TimeStamp</i>.xml". 
    The log file contains one entry per error. Each log entry specifies the:

<ul>
<li>Error code</li>
<li>File name (full path)</li>
<li>Property</li>
<li>Rule applied</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
