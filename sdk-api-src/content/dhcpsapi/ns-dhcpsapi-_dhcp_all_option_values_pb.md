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

# _DHCP_ALL_OPTION_VALUES_PB structure


## -description


The <b>DHCP_ALL_OPTION_VALUES_PB</b> structure defines the set of all option values for a DHCP server within a scope.


## -struct-fields




### -field Flags

Reserved. Must be 0.


### -field NumElements

Integer that specifies the number of elements in <b>Options</b>.


### -field PolicyName

 


### -field VendorName

 


### -field IsVendor

 


### -field OptionsArray

 


### -field size_is

 


### -field size_is.NumElements

 


### -field Options

Pointer to an array of structures that contain the set of all option values for specific vendor/policy pairs. There is one element per pair.



#### PolicyName

Pointer to a null-terminated Unicode string that represents the DHCP server policy name for the option set. <b>NULL</b> if none exists.



#### VendorName

Pointer to a null-terminated Unicode string that represents the vendor name  for the option set. <b>NULL</b> if none exists.



#### IsVendor

<b>TRUE</b> if the option set is vendor-specific. Otherwise, it is <b>FALSE</b>.



#### OptionsArray

A pointer to a <a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the set of all option values for the specified vendor/policy pair.


## -see-also




<a href="https://msdn.microsoft.com/3c2fff2f-3d79-4e0d-8a31-9917088b1413">DhcpV4GetAllOptionValues</a>
 

 

