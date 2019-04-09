---
UID: NF:fsrmpipeline.IFsrmClassificationManager.GetPropertyDefinition
title: IFsrmClassificationManager::GetPropertyDefinition (fsrmpipeline.h)
author: windows-sdk-content
description: Retrieves the specified property definition.
old-location: fsrm\ifsrmclassificationmanager_getpropertydefinition.htm
tech.root: fsrm
ms.assetid: de89524d-70b7-4f0a-add0-d34d54bd32a7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],GetPropertyDefinition method, GetPropertyDefinition, GetPropertyDefinition method [File Server Resource Manager], GetPropertyDefinition method [File Server Resource Manager],FsrmClassificationManager class, GetPropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager interface, GetPropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],GetPropertyDefinition method, IFsrmClassificationManager.GetPropertyDefinition, IFsrmClassificationManager2 interface [File Server Resource Manager],GetPropertyDefinition method, IFsrmClassificationManager2::GetPropertyDefinition, IFsrmClassificationManager::GetPropertyDefinition, fs.ifsrmclassificationmanager_getpropertydefinition, fsrm.ifsrmclassificationmanager_getpropertydefinition, fsrmpipeline/IFsrmClassificationManager2::GetPropertyDefinition, fsrmpipeline/IFsrmClassificationManager::GetPropertyDefinition
ms.topic: method
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
 - IFsrmClassificationManager.GetPropertyDefinition
 - IFsrmClassificationManager2.GetPropertyDefinition
 - FsrmClassificationManager.GetPropertyDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationManager::GetPropertyDefinition


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Retrieves the specified property definition.


## -parameters




### -param propertyName [in]

The name of the property definition to retrieve.


### -param propertyDefinition [out]

An <a href="https://msdn.microsoft.com/b85d5df0-a99a-48d2-9bad-3b8c86abea91">IFsrmPropertyDefinition</a> interface to the 
      retrieved property definition.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/92c6198b-08b6-4ea6-b8de-1a21acd235d1">IFsrmClassificationManager::CreatePropertyDefinition</a>



<a href="https://msdn.microsoft.com/c97cb2f1-6e03-444e-a15e-faa85f7a7915">IFsrmClassificationManager::EnumPropertyDefinitions</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

