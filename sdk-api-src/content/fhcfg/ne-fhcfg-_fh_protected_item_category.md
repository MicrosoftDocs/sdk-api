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

# _FH_PROTECTED_ITEM_CATEGORY enumeration


## -description


Specifies the type of an inclusion or exclusion list.


## -enum-fields




### -field FH_FOLDER

The inclusion or exclusion list is a list of folders.


### -field FH_LIBRARY

The inclusion or exclusion list is a list of libraries.


### -field MAX_PROTECTED_ITEM_CATEGORY

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.


## -remarks



To retrieve the inclusion and exclusion rules that are currently stored in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object, call the <a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a> method.

To add or remove an exclusion rule, call the <a href="https://msdn.microsoft.com/8900944D-3B73-49AB-AE26-F0B2D5842B02">IFhConfigMgr::AddRemoveExcludeRule</a> method.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/8900944D-3B73-49AB-AE26-F0B2D5842B02">IFhConfigMgr::AddRemoveExcludeRule</a>



<a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a>
 

 

