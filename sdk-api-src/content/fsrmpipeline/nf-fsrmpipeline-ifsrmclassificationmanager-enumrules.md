---
UID: NF:fsrmpipeline.IFsrmClassificationManager.EnumRules
title: IFsrmClassificationManager::EnumRules
author: windows-sdk-content
description: Enumerates the rules of the specified type.
old-location: fsrm\ifsrmclassificationmanager_enumrules.htm
old-project: fsrm
ms.assetid: 2f67527c-cde3-4907-9e61-4d9e18b18859
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: EnumRules, EnumRules method [File Server Resource Manager], EnumRules method [File Server Resource Manager],FsrmClassificationManager class, EnumRules method [File Server Resource Manager],IFsrmClassificationManager interface, EnumRules method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],EnumRules method, IFsrmClassificationManager interface [File Server Resource Manager],EnumRules method, IFsrmClassificationManager.EnumRules, IFsrmClassificationManager2 interface [File Server Resource Manager],EnumRules method, IFsrmClassificationManager2::EnumRules, IFsrmClassificationManager::EnumRules, fs.ifsrmclassificationmanager_enumrules, fsrm.ifsrmclassificationmanager_enumrules, fsrmpipeline/IFsrmClassificationManager2::EnumRules, fsrmpipeline/IFsrmClassificationManager::EnumRules
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
 - IFsrmClassificationManager.EnumRules
 - IFsrmClassificationManager2.EnumRules
 - FsrmClassificationManager.EnumRules
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::EnumRules


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Enumerates the rules of the specified type.


## -parameters




### -param ruleType [in]

The type of rules to enumerate. For possible values, see the 
       <a href="https://msdn.microsoft.com/9fd9daf2-5e3e-4d9c-8f19-92e31756a1c7">FsrmRuleType</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmRuleType_Generic</b> type is not a valid type for this method.</div>
<div> </div>

### -param options [in]

One or more options for enumerating the property definitions. For possible values, see the 
       <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmEnumOptions_Asynchronous</b> option is not supported for this 
       method.</div>
<div> </div>

### -param Rules






#### - rules [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a 
       collection of classification rules. Each item in the collection is a <b>VARIANT</b> of 
       type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant 
       for the <a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a> interface. You can then use the 
       <a href="https://msdn.microsoft.com/a1aa2c94-b2f0-4620-8589-27360f5bdf05">IFsrmRule.RuleType</a> property to determine the rule's 
       type. Query the <b>IFsrmRule</b> interface for the rule interface to 
       use. For example, if <b>RuleType</b> is 
       <b>FsrmRuleType_Classification</b>, query the 
       <b>IFsrmRule</b> interface for the 
       <a href="https://msdn.microsoft.com/d76e4b07-66d6-426f-853d-f52ea08d9b81">IFsrmClassificationRule</a> interface.

The collection contains only committed rules; the collection will not contain newly created rules that have 
       not been committed.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/ca9a97b7-eadd-4f57-8f3a-afa439222f21">IFsrmClassificationManager::CreateRule</a>



<a href="https://msdn.microsoft.com/2c21ed09-6c69-4f03-91bb-9beeb816ed62">IFsrmClassificationManager::GetRule</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

