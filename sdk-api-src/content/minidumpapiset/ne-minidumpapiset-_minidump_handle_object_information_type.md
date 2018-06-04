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

# _MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE enumeration


## -description


Identifies the type of object-specific information.


## -enum-fields




### -field MiniHandleObjectInformationNone

There is no object-specific information for this handle type.


### -field MiniThreadInformation1

The information is specific to thread objects.


### -field MiniMutantInformation1

The information is specific to mutant objects.


### -field MiniMutantInformation2

The information is specific to mutant objects.


### -field MiniProcessInformation1

The information is specific to process objects.


### -field MiniProcessInformation2

The information is specific to process objects.


### -field MiniEventInformation1


### -field MiniSectionInformation1


### -field MiniSemaphoreInformation1


### -field MiniHandleObjectInformationTypeMax




## -remarks



The information represented by each of these values can vary by operating system and procesor architecture. Per-handle object-specific information is automatically gathered when minidump type is MiniDumpWithHandleData. For more information, see <a href="https://msdn.microsoft.com/89ae3a75-5f02-4c5e-9d72-95fb8ef94985">MINIDUMP_TYPE</a>.




## -see-also




<a href="https://msdn.microsoft.com/fb79de10-7a98-4a21-b394-63e5279b6681">MINIDUMP_HANDLE_OBJECT_INFORMATION</a>
 

 

