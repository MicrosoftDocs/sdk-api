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

# _MAPPING_PROPERTY_BAG structure


## -description



Contains the text recognition data properties retrieved by <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.




## -struct-fields




### -field Size

Size of the structure, used to verify the structure version. This value is required.


### -field prgResultRanges

Pointer to an array of <a href="https://msdn.microsoft.com/adff7901-1903-45dd-888f-1b8c5bb05de1">MAPPING_DATA_RANGE</a> structures containing all recognized text range results. This member is populated by <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.


### -field dwRangesCount

Number of items in the array indicated by <b>prgResultRanges</b>. This member is populated by <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.


### -field pServiceData

Pointer to private service data. The service can document the format of this data so that the application can use it. The service also manages the memory for this data. This member is populated by <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.


### -field dwServiceDataSize

Size, in bytes, of the private service data specified by <b>pServiceData</b>. The size is set to 0 if there is no private data. This member is populated by <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.


### -field pCallerData

Pointer to private application data to pass to the service. The application manages the memory for this data.


### -field dwCallerDataSize

Size, in bytes, of the private application data indicated in <b>pCallerData</b>. This member is set to 0 if there is no private data.


### -field pContext

Reserved for internal use.


## -remarks



The memory for the property bag structure itself is managed by the application. The ELS platform and its services only manage the data pointers that they store in the property bag.




## -see-also




<a href="https://msdn.microsoft.com/58cdccf8-f052-4bb3-9391-2cc537d820dd">Extended Linguistic Services Structures</a>



<a href="https://msdn.microsoft.com/adff7901-1903-45dd-888f-1b8c5bb05de1">MAPPING_DATA_RANGE</a>



<a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>
 

 

