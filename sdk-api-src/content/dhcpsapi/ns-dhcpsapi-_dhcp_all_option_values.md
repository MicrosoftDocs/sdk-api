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

# _DHCP_ALL_OPTION_VALUES structure


## -description


The <b>DHCP_ALL_OPTION_VALUES</b> structure defines the set of all option values defined on a DHCP server, organized according to class/vendor pairing.


## -struct-fields




### -field Flags

Reserved. This field should be set to 0.


### -field NumElements

Specifies the number of elements in <b>Options</b>.


### -field ClassName

 


### -field VendorName

 


### -field IsVendor

 


### -field OptionsArray

 


### -field size_is

 


### -field size_is.NumElements

 


### -field Options

 




#### - *Options

Pointer to a list of structures that contain the option values for specific class/vendor pairs. The structure is defined as follows.



#### ClassName

Unicode string that contains the name of the DHCP class for the option list.



#### VendorName

Unicode string that contains the name of the vendor for the option list.



#### IsVendor

Specifies whether or not this set of options is vendor-specific. This value is <b>TRUE</b> if it is, and <b>FALSE</b> if it is not.



#### OptionsArray


<a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the option values for the specified vendor/class pair.

