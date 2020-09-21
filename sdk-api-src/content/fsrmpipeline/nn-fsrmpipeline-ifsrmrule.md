---
UID: NN:fsrmpipeline.IFsrmRule
title: IFsrmRule (fsrmpipeline.h)
description: Defines a rule.
helpviewer_keywords: ["IFsrmRule","IFsrmRule interface [File Server Resource Manager]","IFsrmRule interface [File Server Resource Manager]","described","fs.ifsrmrule","fsrm.ifsrmrule","fsrm/IFsrmRule"]
old-location: fsrm\ifsrmrule.htm
tech.root: fsrm
ms.assetid: e1de871f-a2c9-4787-a3e8-8c3428e9249e
ms.date: 12/05/2018
ms.keywords: IFsrmRule, IFsrmRule interface [File Server Resource Manager], IFsrmRule interface [File Server Resource Manager],described, fs.ifsrmrule, fsrm.ifsrmrule, fsrm/IFsrmRule
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
 - IFsrmRule
 - fsrmpipeline/IFsrmRule
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
 - IFsrmRule
---

# IFsrmRule interface


## -description

Defines a rule.

To create a rule, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createrule">IFsrmClassificationManager::CreateRule</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumrules">IFsrmClassificationManager::EnumRules</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getrule">IFsrmClassificationManager::GetRule</a>
</li>
</ul>This is the base class for rule interfaces. Query this interface to get the interface for the rule type 
    specified in the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmrule-get_ruletype">RuleType</a> property. For example, if 
    <b>RuleType</b> is 
    <b>FsrmRuleType_Classification</b>, query this interface for the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationrule">IFsrmClassificationRule</a> interface.

## -remarks

The name and rule type properties define a unique rule.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationrule">IFsrmClassificationRule</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>