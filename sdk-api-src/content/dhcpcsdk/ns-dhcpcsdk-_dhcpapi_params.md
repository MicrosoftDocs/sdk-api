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

# _DHCPAPI_PARAMS structure


## -description


The <b>DHCPAPI_PARAMS</b> structure is used to request DHCP parameters.


## -struct-fields




### -field Flags

Reserved. Must be set to zero.


### -field OptionId

Identifier for the DHCP parameter being requested.


### -field IsVendor

Specifies whether the DHCP parameter is vendor-specific. Set to <b>TRUE</b> if the parameter is vendor-specific.


### -field Data.size_is

 


### -field Data.size_is.nBytesData

 


### -field Data

Pointer to the parameter data.


### -field nBytesData

Size of the data pointed to by <b>Data</b>, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/84eafc6b-e9ee-4c73-b872-b2abc7e257df">DHCPAPI_PARAMS_ARRAY</a>
 

 

