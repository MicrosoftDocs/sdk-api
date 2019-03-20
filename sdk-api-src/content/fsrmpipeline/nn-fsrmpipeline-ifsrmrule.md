---
UID: NN:fsrmpipeline.IFsrmRule
title: IFsrmRule (fsrmpipeline.h)
author: windows-sdk-content
description: Defines a rule.
old-location: fsrm\ifsrmrule.htm
tech.root: fsrm
ms.assetid: e1de871f-a2c9-4787-a3e8-8c3428e9249e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmRule, IFsrmRule interface [File Server Resource Manager], IFsrmRule interface [File Server Resource Manager],described, fs.ifsrmrule, fsrm.ifsrmrule, fsrm/IFsrmRule
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmRule interface


## -description


Defines a rule.

To create a rule, call the 
    <a href="https://msdn.microsoft.com/ca9a97b7-eadd-4f57-8f3a-afa439222f21">IFsrmClassificationManager::CreateRule</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/2f67527c-cde3-4907-9e61-4d9e18b18859">IFsrmClassificationManager::EnumRules</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2c21ed09-6c69-4f03-91bb-9beeb816ed62">IFsrmClassificationManager::GetRule</a>
</li>
</ul>This is the base class for rule interfaces. Query this interface to get the interface for the rule type 
    specified in the <a href="https://msdn.microsoft.com/a1aa2c94-b2f0-4620-8589-27360f5bdf05">RuleType</a> property. For example, if 
    <b>RuleType</b> is 
    <b>FsrmRuleType_Classification</b>, query this interface for the 
    <a href="https://msdn.microsoft.com/d76e4b07-66d6-426f-853d-f52ea08d9b81">IFsrmClassificationRule</a> interface.


## -remarks



The name and rule type properties define a unique rule.




## -see-also




<a href="https://msdn.microsoft.com/d76e4b07-66d6-426f-853d-f52ea08d9b81">IFsrmClassificationRule</a>



<a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>
 

 

