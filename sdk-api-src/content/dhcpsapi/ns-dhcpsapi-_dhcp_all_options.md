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

# _DHCP_ALL_OPTIONS structure


## -description


The <b>DHCP_ALL_OPTIONS</b> structure defines the set of all options available on a DHCP server.


## -struct-fields




### -field Flags

Reserved. This value should be set to 0.


### -field NonVendorOptions


<a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a> structure that contains the set of non-vendor options.


### -field NumVendorOptions

Specifies the number of vendor options listed in <b>VendorOptions</b>.


### -field Option

 


### -field VendorName

 


### -field ClassName

 


### -field size_is

 


### -field size_is.NumVendorOptions

 


### -field VendorOptions

 




#### - *VendorOptions

Pointer to a list of structures that contain the following fields.



#### Option


<a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">DHCP_OPTION</a> structure that contains specific information describing the option.



#### VendorName

Unicode string that contains the name of the vendor for the option.



#### ClassName

Unicode string that contains the name of the DHCP class for the option.

