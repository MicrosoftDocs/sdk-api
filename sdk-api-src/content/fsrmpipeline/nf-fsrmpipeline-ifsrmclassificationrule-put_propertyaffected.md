---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

