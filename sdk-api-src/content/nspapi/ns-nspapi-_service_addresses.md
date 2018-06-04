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

# _SERVICE_ADDRESSES structure


## -description



			The 
<b>SERVICE_ADDRESSES</b> structure contains an array of 
<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a> data structures.


## -struct-fields




### -field dwAddressCount

Number of 
<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a> structures in the <b>Addresses</b> array.


### -field Addressses

 


### -field Addressses.size_is

 


### -field Addressses.size_is.dwAddressCount

 


### -field Addresses

Array of 
<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a> data structures. Each 
<b>SERVICE_ADDRESS</b> structure contains information about a network service address.


## -see-also




<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a>



<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a>
 

 

