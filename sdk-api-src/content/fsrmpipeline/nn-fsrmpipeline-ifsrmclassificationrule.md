---
UID: NN:fsrmpipeline.IFsrmClassificationRule
title: IFsrmClassificationRule
author: windows-sdk-content
description: Defines a classification rule.
old-location: fsrm\ifsrmclassificationrule.htm
tech.root: fsrm
ms.assetid: d76e4b07-66d6-426f-853d-f52ea08d9b81
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmClassificationRule, IFsrmClassificationRule interface [File Server Resource Manager], IFsrmClassificationRule interface [File Server Resource Manager],described, fs.ifsrmclassificationrule, fsrm.ifsrmclassificationrule, fsrm/IFsrmClassificationRule
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmClassificationRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationRule interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/845fc1e8-d06a-4bc4-9529-0748cb488727">MSFT_FSRMClassificationRule</a> class.]

Defines a classification rule. The rule defines the paths to which the rule applies, the 
    classifier module to run on files in those paths, and the property and property value used to classify each 
    file.

To create a classification rule, call the 
    <a href="https://msdn.microsoft.com/ca9a97b7-eadd-4f57-8f3a-afa439222f21">IFsrmClassificationManager::CreateRule</a> 
    method.

The following methods can return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/2f67527c-cde3-4907-9e61-4d9e18b18859">IFsrmClassificationManager::EnumRules</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2c21ed09-6c69-4f03-91bb-9beeb816ed62">IFsrmClassificationManager::GetRule</a>
</li>
</ul>

## -remarks



The rule runs when you call the 
    <a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a> 
    method. You can also schedule the classification process to run on a specified schedule.




## -see-also




<a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a>



<a href="https://msdn.microsoft.com/845fc1e8-d06a-4bc4-9529-0748cb488727">MSFT_FSRMClassificationRule</a>
 

 

