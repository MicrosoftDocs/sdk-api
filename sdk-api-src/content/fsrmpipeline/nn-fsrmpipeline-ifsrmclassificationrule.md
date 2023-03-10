---
UID: NN:fsrmpipeline.IFsrmClassificationRule
title: IFsrmClassificationRule (fsrmpipeline.h)
description: Defines a classification rule.
helpviewer_keywords: ["IFsrmClassificationRule","IFsrmClassificationRule interface [File Server Resource Manager]","IFsrmClassificationRule interface [File Server Resource Manager]","described","fs.ifsrmclassificationrule","fsrm.ifsrmclassificationrule","fsrm/IFsrmClassificationRule"]
old-location: fsrm\ifsrmclassificationrule.htm
tech.root: fsrm
ms.assetid: d76e4b07-66d6-426f-853d-f52ea08d9b81
ms.date: 12/05/2018
ms.keywords: IFsrmClassificationRule, IFsrmClassificationRule interface [File Server Resource Manager], IFsrmClassificationRule interface [File Server Resource Manager],described, fs.ifsrmclassificationrule, fsrm.ifsrmclassificationrule, fsrm/IFsrmClassificationRule
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmClassificationRule
 - fsrmpipeline/IFsrmClassificationRule
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
 - IFsrmClassificationRule
---

# IFsrmClassificationRule interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassificationrule">MSFT_FSRMClassificationRule</a> class.]

Defines a classification rule. The rule defines the paths to which the rule applies, the 
    classifier module to run on files in those paths, and the property and property value used to classify each 
    file.

To create a classification rule, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createrule">IFsrmClassificationManager::CreateRule</a> 
    method.

The following methods can return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumrules">IFsrmClassificationManager::EnumRules</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getrule">IFsrmClassificationManager::GetRule</a>
</li>
</ul>

## -remarks

The rule runs when you call the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">IFsrmClassificationManager::RunClassification</a> 
    method. You can also schedule the classification process to run on a specified schedule.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassificationrule">MSFT_FSRMClassificationRule</a>