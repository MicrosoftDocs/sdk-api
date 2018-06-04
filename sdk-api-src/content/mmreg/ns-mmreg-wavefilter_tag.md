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

# wavefilter_tag structure


## -description



The <b>WAVEFILTER</b> structure defines a filter for waveform-audio data. Only filter information common to all waveform-audio data filters is included in this structure. For filters that require additional information, this structure is included as the first member in another structure along with the additional information.




## -struct-fields




### -field cbStruct

Size, in bytes, of the <b>WAVEFILTER</b> structure. The size specified in this member must be large enough to contain the base <b>WAVEFILTER</b> structure.


### -field dwFilterTag

Waveform-audio filter type. Filter tags are registered with Microsoft Corporation for various filter algorithms.


### -field fdwFilter

Flags for the <b>dwFilterTag</b> member. The flags defined for this member are universal to all filters. Currently, no flags are defined.


### -field dwReserved

Reserved for system use; should not be examined or modified by an application.


## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/4ae84ba8-f444-4d9e-adc8-343b4ee764cc">Waveform Structures</a>
 

 

