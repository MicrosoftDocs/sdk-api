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

# _MESSAGE_RESOURCE_DATA structure


## -description


Contains information about formatted text for display as an error message or in a message box in a message table resource. 


## -struct-fields




### -field NumberOfBlocks

Type: <b>DWORD</b>

The number of <a href="https://msdn.microsoft.com/573f22be-d204-4c0d-9c45-bd6d46094e32">MESSAGE_RESOURCE_BLOCK</a> structures. 


### -field Blocks

Type: <b><a href="https://msdn.microsoft.com/573f22be-d204-4c0d-9c45-bd6d46094e32">MESSAGE_RESOURCE_BLOCK</a>[1]</b>

An array of structures. The array is the size indicated by the 
					<b>NumberOfBlocks</b>  member. 


## -remarks



A <b>MESSAGE_RESOURCE_DATA</b> structure can contain one or more 
				<a href="https://msdn.microsoft.com/573f22be-d204-4c0d-9c45-bd6d46094e32">MESSAGE_RESOURCE_BLOCK</a> structures, which can each contain one or more <a href="https://msdn.microsoft.com/cce13b09-5c8b-4d64-a229-419d01d91f27">MESSAGE_RESOURCE_ENTRY</a> structures. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/573f22be-d204-4c0d-9c45-bd6d46094e32">MESSAGE_RESOURCE_BLOCK</a>



<a href="https://msdn.microsoft.com/cce13b09-5c8b-4d64-a229-419d01d91f27">MESSAGE_RESOURCE_ENTRY</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

