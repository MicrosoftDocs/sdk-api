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

# IUpdate2::get_IsPresent


## -description


Gets a Boolean value that indicates whether an update is present on a computer.

This property is read-only.


## -parameters


## -remarks



An update is considered present if it is installed for one or more products. For example, if an update applies to both Microsoft Office Word and to Microsoft Office Excel, the <b>IsPresent</b> property returns <b>VARIANT_TRUE</b> if the update is installed for one or both of the products.

If an update applies to only one product, the <b>IsPresent</b> and <a href="https://msdn.microsoft.com/2adebe8e-554e-4337-9bbf-1d8967fefef1">IsInstalled</a> properties are equivalent. An update is considered installed if the update is installed for all the products to which it applies.

If <b>IsPresent</b> returns <b>VARIANT_TRUE</b> and <a href="https://msdn.microsoft.com/2adebe8e-554e-4337-9bbf-1d8967fefef1">IsInstalled</a> returns <b>VARIANT_FALSE</b>, the update can be uninstalled for the product that installed it.




## -see-also




<a href="https://msdn.microsoft.com/75041e85-0f3c-4996-9af2-d2969549393e">IUpdate2</a>
 

 

