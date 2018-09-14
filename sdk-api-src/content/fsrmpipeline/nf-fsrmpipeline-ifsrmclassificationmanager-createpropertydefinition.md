---
UID: NF:fsrmpipeline.IFsrmClassificationManager.CreatePropertyDefinition
title: IFsrmClassificationManager::CreatePropertyDefinition
author: windows-sdk-content
description: Creates a property definition.
old-location: fsrm\ifsrmclassificationmanager_createpropertydefinition.htm
tech.root: fsrm
ms.assetid: 92c6198b-08b6-4ea6-b8de-1a21acd235d1
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: CreatePropertyDefinition, CreatePropertyDefinition method [File Server Resource Manager], CreatePropertyDefinition method [File Server Resource Manager],FsrmClassificationManager class, CreatePropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager interface, CreatePropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],CreatePropertyDefinition method, IFsrmClassificationManager interface [File Server Resource Manager],CreatePropertyDefinition method, IFsrmClassificationManager.CreatePropertyDefinition, IFsrmClassificationManager2 interface [File Server Resource Manager],CreatePropertyDefinition method, IFsrmClassificationManager2::CreatePropertyDefinition, IFsrmClassificationManager::CreatePropertyDefinition, fs.ifsrmclassificationmanager_createpropertydefinition, fsrm.ifsrmclassificationmanager_createpropertydefinition, fsrmpipeline/IFsrmClassificationManager2::CreatePropertyDefinition, fsrmpipeline/IFsrmClassificationManager::CreatePropertyDefinition
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
 - IFsrmClassificationManager.CreatePropertyDefinition
 - IFsrmClassificationManager2.CreatePropertyDefinition
 - FsrmClassificationManager.CreatePropertyDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationManager::CreatePropertyDefinition


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Creates a property definition.


## -parameters




### -param propertyDefinition [out]

An <a href="https://msdn.microsoft.com/b85d5df0-a99a-48d2-9bad-3b8c86abea91">IFsrmPropertyDefinition</a> interface to the 
      new property definition. To save the property definition, call 
      <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmPropertyDefinition::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



You create a property definition to define the property that you want to use to classify files. One or more 
    classification rules can specify the property. The FSRM server limits the number of property definitions to 
    100.

You cannot delete a property that is referenced by a rule or report job.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/c97cb2f1-6e03-444e-a15e-faa85f7a7915">IFsrmClassificationManager::EnumPropertyDefinitions</a>



<a href="https://msdn.microsoft.com/de89524d-70b7-4f0a-add0-d34d54bd32a7">IFsrmClassificationManager::GetPropertyDefinition</a>



<a href="https://msdn.microsoft.com/0e41ac2b-c48a-4bb8-a363-8a64c856b8f9">IFsrmClassificationRule::PropertyAffected</a>



<b>MSFT_FSRMClassification</b>
 

 

