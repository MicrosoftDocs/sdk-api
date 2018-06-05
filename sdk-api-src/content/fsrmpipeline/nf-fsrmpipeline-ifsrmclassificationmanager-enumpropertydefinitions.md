---
UID: NF:fsrmpipeline.IFsrmClassificationManager.EnumPropertyDefinitions
title: IFsrmClassificationManager::EnumPropertyDefinitions
author: windows-sdk-content
description: Enumerates the property definitions.
old-location: fsrm\ifsrmclassificationmanager_enumpropertydefinitions.htm
old-project: Fsrm
ms.assetid: c97cb2f1-6e03-444e-a15e-faa85f7a7915
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: EnumPropertyDefinitions, EnumPropertyDefinitions method [File Server Resource Manager], EnumPropertyDefinitions method [File Server Resource Manager],FsrmClassificationManager class, EnumPropertyDefinitions method [File Server Resource Manager],IFsrmClassificationManager interface, EnumPropertyDefinitions method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],EnumPropertyDefinitions method, IFsrmClassificationManager interface [File Server Resource Manager],EnumPropertyDefinitions method, IFsrmClassificationManager.EnumPropertyDefinitions, IFsrmClassificationManager2 interface [File Server Resource Manager],EnumPropertyDefinitions method, IFsrmClassificationManager2::EnumPropertyDefinitions, IFsrmClassificationManager::EnumPropertyDefinitions, fs.ifsrmclassificationmanager_enumpropertydefinitions, fsrm.ifsrmclassificationmanager_enumpropertydefinitions, fsrmpipeline/IFsrmClassificationManager2::EnumPropertyDefinitions, fsrmpipeline/IFsrmClassificationManager::EnumPropertyDefinitions
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmClassificationManager.EnumPropertyDefinitions
-	IFsrmClassificationManager2.EnumPropertyDefinitions
-	FsrmClassificationManager.EnumPropertyDefinitions
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::EnumPropertyDefinitions


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Enumerates the property definitions.


## -parameters




### -param options [in]

One or more options for enumerating the property definitions. For possible values, see the 
      <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param propertyDefinitions [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a 
       collection of property definitions. Each item in the collection is a <b>VARIANT</b> of 
       type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the 
       variant for the <a href="https://msdn.microsoft.com/b85d5df0-a99a-48d2-9bad-3b8c86abea91">IFsrmPropertyDefinition</a> 
       interface.

The collection contains only committed property definitions; the collection will not contain newly created 
       property definitions that have not been committed.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/92c6198b-08b6-4ea6-b8de-1a21acd235d1">IFsrmClassificationManager::CreatePropertyDefinition</a>



<a href="https://msdn.microsoft.com/de89524d-70b7-4f0a-add0-d34d54bd32a7">IFsrmClassificationManager::GetPropertyDefinition</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

