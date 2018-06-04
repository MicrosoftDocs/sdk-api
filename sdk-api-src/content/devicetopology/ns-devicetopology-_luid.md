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

# _LUID structure


## -description


The <b>LUID</b> structure stores the video port identifier. This structure is stored in the <b>PortId</b> member of the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff537140">KSJACK_SINK_INFORMATION</a> structure.


## -struct-fields




### -field LowPart

LowPart of the video port identifier.


### -field HighPart

HighPart of the video port identifier. 


## -see-also




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/ca4165ce-433a-4a8f-9853-bbe812de90ca">IKsJackSinkInformation::GetJackSinkInformation</a>
 

 

