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

# _DHCP_POL_COND structure


## -description


The <b>DHCP_POL_COND</b> structure defines the DHCP server policy condition.


## -struct-fields




### -field ParentExpr

Integer that specifies the expression index that corresponds to this constituent condition.


### -field Type


<a href="https://msdn.microsoft.com/02a84c55-402c-40fe-8dad-6ed3f58052a1">DHCP_POL_ATTR_TYPE</a> enumeration that specifies the attribute type for this condition.


### -field OptionID


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the unique option identifier for criteria based on DHCP options or sub-options.


### -field SubOptionID


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the unique sub-option identifier.


### -field VendorName

A pointer to a null-terminated Unicode string that represents the vendor name.


### -field Operator


<a href="https://msdn.microsoft.com/7b34e9ec-a3c6-4b85-bb36-d4f834912a64">DHCP_POL_COMPARATOR</a> enumeration that specifies the comparison operator for the condition.


### -field Value

Pointer to an array of bytes that contains the value to be used for the comparison.


### -field Value.size_is

 


### -field Value.size_is.ValueLength

 


### -field ValueLength

Integer that specifies the length of <b>Value</b>.


## -see-also




<a href="https://msdn.microsoft.com/2A084E80-92F8-43F5-89C8-22F08CE449E9">DHCP_POL_COND_ARRAY</a>
 

 

