---
UID: NF:fsrmpipeline.IFsrmRule.get_RuleType
title: IFsrmRule::get_RuleType
author: windows-sdk-content
description: The type of the rule.
old-location: fsrm\ifsrmrule_ruletype.htm
tech.root: Fsrm
ms.assetid: a1aa2c94-b2f0-4620-8589-27360f5bdf05
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],RuleType property, IFsrmRule.RuleType, IFsrmRule.get_RuleType, IFsrmRule::RuleType, IFsrmRule::get_RuleType, RuleType property [File Server Resource Manager], RuleType property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_ruletype, fsrm.ifsrmrule_ruletype, fsrmpipeline/IFsrmRule::RuleType, fsrmpipeline/IFsrmRule::get_RuleType, get_RuleType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmRule::get_RuleType


## -description


The type of the rule.

This property is read-only.


## -parameters


## -remarks



The rule's type is specified when you call the <a href="https://msdn.microsoft.com/ca9a97b7-eadd-4f57-8f3a-afa439222f21">IFsrmClassificationManager::CreateRule</a> method to create the rule.

The name and rule type properties define a unique rule.




## -see-also




<a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a>
 

 

