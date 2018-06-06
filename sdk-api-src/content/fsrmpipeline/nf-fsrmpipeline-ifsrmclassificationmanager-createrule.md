---
UID: NF:fsrmpipeline.IFsrmClassificationManager.CreateRule
title: IFsrmClassificationManager::CreateRule
author: windows-sdk-content
description: Creates a rule of the specified type.
old-location: fsrm\ifsrmclassificationmanager_createrule.htm
old-project: Fsrm
ms.assetid: ca9a97b7-eadd-4f57-8f3a-afa439222f21
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: CreateRule, CreateRule method [File Server Resource Manager], CreateRule method [File Server Resource Manager],FsrmClassificationManager class, CreateRule method [File Server Resource Manager],IFsrmClassificationManager interface, CreateRule method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],CreateRule method, IFsrmClassificationManager interface [File Server Resource Manager],CreateRule method, IFsrmClassificationManager.CreateRule, IFsrmClassificationManager2 interface [File Server Resource Manager],CreateRule method, IFsrmClassificationManager2::CreateRule, IFsrmClassificationManager::CreateRule, fs.ifsrmclassificationmanager_createrule, fsrm.ifsrmclassificationmanager_createrule, fsrmpipeline/IFsrmClassificationManager2::CreateRule, fsrmpipeline/IFsrmClassificationManager::CreateRule
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmClassificationManager.CreateRule
 - IFsrmClassificationManager2.CreateRule
 - FsrmClassificationManager.CreateRule
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::CreateRule


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Creates a rule of the specified type.


## -parameters




### -param ruleType [in]

The type of rule to create, set this parameter to <b>FsrmRuleType_Classification</b>. 
      For more information, see <a href="https://msdn.microsoft.com/9fd9daf2-5e3e-4d9c-8f19-92e31756a1c7">FsrmRuleType</a>.


### -param Rule






#### - rule [out]

An <a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a> interface to the new rule. Query the 
       <b>IFsrmRule</b> interface to get the interface to get the 
       <a href="https://msdn.microsoft.com/d76e4b07-66d6-426f-853d-f52ea08d9b81">IFsrmClassificationRule</a> interface.

To save the rule, call <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmRule::Commit</a> 
       method.


## -returns



The method returns the following return values.




## -remarks



There is no limit to the number of rules that you can create. Use the 
    <a href="https://msdn.microsoft.com/b003b31b-fe40-446d-9db8-619dfcecc6c7">IFsrmRule.ModuleDefinitionName</a> property 
    to associate the rule with a classification module.

FSRM cannot guarantee the order in which the rules 
    are run.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/2f67527c-cde3-4907-9e61-4d9e18b18859">IFsrmClassificationManager::EnumRules</a>



<a href="https://msdn.microsoft.com/2c21ed09-6c69-4f03-91bb-9beeb816ed62">IFsrmClassificationManager::GetRule</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

