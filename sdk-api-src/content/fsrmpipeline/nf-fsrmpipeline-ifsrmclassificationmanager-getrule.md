---
UID: NF:fsrmpipeline.IFsrmClassificationManager.GetRule
title: IFsrmClassificationManager::GetRule
author: windows-sdk-content
description: Retrieves the specified rule.
old-location: fsrm\ifsrmclassificationmanager_getrule.htm
tech.root: Fsrm
ms.assetid: 2c21ed09-6c69-4f03-91bb-9beeb816ed62
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],GetRule method, GetRule, GetRule method [File Server Resource Manager], GetRule method [File Server Resource Manager],FsrmClassificationManager class, GetRule method [File Server Resource Manager],IFsrmClassificationManager interface, GetRule method [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],GetRule method, IFsrmClassificationManager.GetRule, IFsrmClassificationManager2 interface [File Server Resource Manager],GetRule method, IFsrmClassificationManager2::GetRule, IFsrmClassificationManager::GetRule, fs.ifsrmclassificationmanager_getrule, fsrm.ifsrmclassificationmanager_getrule, fsrmpipeline/IFsrmClassificationManager2::GetRule, fsrmpipeline/IFsrmClassificationManager::GetRule
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmClassificationManager.GetRule
 - IFsrmClassificationManager2.GetRule
 - FsrmClassificationManager.GetRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmpipeline.h
: 
- IFsrmClassificationManager.GetRule
: 
---

# IFsrmClassificationManager::GetRule


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Retrieves the specified rule.


## -parameters




### -param ruleName [in]

The name of the rule to retrieve. Must not exceed 100 characters in length.


### -param ruleType [in]

The type of the rule to retrieve. For possible types, see the 
       <a href="https://msdn.microsoft.com/9fd9daf2-5e3e-4d9c-8f19-92e31756a1c7">FsrmRuleType</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmRuleType_Generic</b> type is not supported by this method.</div>
<div> </div>

### -param Rule [out]

An <a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a> interface to  the retrieved rule. Query the 
      <b>IFsrmRule</b> interface to get the interface for the specified 
      type. For example, if <i>ruleType</i> is 
      <b>FsrmRuleType_Classification</b>, query the 
      <b>IFsrmRule</b> interface for the 
      <a href="https://msdn.microsoft.com/d76e4b07-66d6-426f-853d-f52ea08d9b81">IFsrmClassificationRule</a> interface.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/ca9a97b7-eadd-4f57-8f3a-afa439222f21">IFsrmClassificationManager::CreateRule</a>



<a href="https://msdn.microsoft.com/2f67527c-cde3-4907-9e61-4d9e18b18859">IFsrmClassificationManager::EnumRules</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

