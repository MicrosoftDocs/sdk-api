---
UID: NF:fsrmpipeline.IFsrmClassificationRule.put_PropertyAffected
title: IFsrmClassificationRule::put_PropertyAffected (fsrmpipeline.h)
author: windows-sdk-content
description: The name of the property that this rule affects.
old-location: fsrm\ifsrmclassificationrule_propertyaffected.htm
tech.root: fsrm
ms.assetid: 0e41ac2b-c48a-4bb8-a363-8a64c856b8f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmClassificationRule interface [File Server Resource Manager],PropertyAffected property, IFsrmClassificationRule.PropertyAffected, IFsrmClassificationRule.put_PropertyAffected, IFsrmClassificationRule::PropertyAffected, IFsrmClassificationRule::get_PropertyAffected, IFsrmClassificationRule::put_PropertyAffected, PropertyAffected property [File Server Resource Manager], PropertyAffected property [File Server Resource Manager],IFsrmClassificationRule interface, fs.ifsrmclassificationrule_propertyaffected, fsrm.ifsrmclassificationrule_propertyaffected, fsrmpipeline/IFsrmClassificationRule::PropertyAffected, fsrmpipeline/IFsrmClassificationRule::get_PropertyAffected, fsrmpipeline/IFsrmClassificationRule::put_PropertyAffected, put_PropertyAffected
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
 - IFsrmClassificationRule.PropertyAffected
 - IFsrmClassificationRule.get_PropertyAffected
 - IFsrmClassificationRule.put_PropertyAffected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationRule::put_PropertyAffected


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/845fc1e8-d06a-4bc4-9529-0748cb488727">MSFT_FSRMClassificationRule</a> class.]

The name of the property that this rule affects.

This property is read/write.


## -parameters


## -remarks



If the classifier specifies a list of properties that it affects (see 
    <a href="https://msdn.microsoft.com/69f288d1-cc78-4af0-891b-c5c3ed8d2659">IFsrmClassifierModuleDefinition::PropertiesAffected</a>), the property that you specify must exist in the list of affected properties.

To enumerate the properties that have been defined, call the <a href="https://msdn.microsoft.com/c97cb2f1-6e03-444e-a15e-faa85f7a7915">IFsrmClassificationManager::EnumPropertyDefinitions</a> method. To access the name of the property, use the <a href="https://msdn.microsoft.com/b6c72b75-ef12-4f66-91dc-460d2de8072d">IFsrmPropertyDefinition.Name</a> 
    property.




## -see-also




<a href="https://msdn.microsoft.com/d76e4b07-66d6-426f-853d-f52ea08d9b81">IFsrmClassificationRule</a>



<a href="https://msdn.microsoft.com/845fc1e8-d06a-4bc4-9529-0748cb488727">MSFT_FSRMClassificationRule</a>
 

 

