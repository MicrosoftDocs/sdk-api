---
UID: NF:fsrmpipeline.IFsrmRule.get_RuleType
title: IFsrmRule::get_RuleType (fsrmpipeline.h)
description: The type of the rule.
helpviewer_keywords: ["IFsrmRule interface [File Server Resource Manager]","RuleType property","IFsrmRule.RuleType","IFsrmRule.get_RuleType","IFsrmRule::RuleType","IFsrmRule::get_RuleType","RuleType property [File Server Resource Manager]","RuleType property [File Server Resource Manager]","IFsrmRule interface","fs.ifsrmrule_ruletype","fsrm.ifsrmrule_ruletype","fsrmpipeline/IFsrmRule::RuleType","fsrmpipeline/IFsrmRule::get_RuleType","get_RuleType"]
old-location: fsrm\ifsrmrule_ruletype.htm
tech.root: fsrm
ms.assetid: a1aa2c94-b2f0-4620-8589-27360f5bdf05
ms.date: 12/05/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],RuleType property, IFsrmRule.RuleType, IFsrmRule.get_RuleType, IFsrmRule::RuleType, IFsrmRule::get_RuleType, RuleType property [File Server Resource Manager], RuleType property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_ruletype, fsrm.ifsrmrule_ruletype, fsrmpipeline/IFsrmRule::RuleType, fsrmpipeline/IFsrmRule::get_RuleType, get_RuleType
req.header: fsrmpipeline.h
req.include-header: 
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
 - IFsrmRule::get_RuleType
 - fsrmpipeline/IFsrmRule::get_RuleType
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
 - IFsrmRule.RuleType
 - IFsrmRule.get_RuleType
---

# IFsrmRule::get_RuleType


## -description

The type of the rule.

This property is read-only.

## -parameters

## -remarks

The rule's type is specified when you call the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createrule">IFsrmClassificationManager::CreateRule</a> method to create the rule.

The name and rule type properties define a unique rule.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a>