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

# tagVMRGUID structure


## -description



The <code>VMRGUID</code> structure is a member of the <a href="https://msdn.microsoft.com/87567836-c01e-4615-a8e7-9ca590b6f7c9">VMRMONITORINFO</a> structure and is used to identify a monitor on the system (VMR-7 only).




## -struct-fields




### -field pGUID

Pointer to the GUID member of the structure. <b>pGUID</b> is <b>NULL</b> if the monitor is the default DirectDraw device.


### -field GUID

Specifies the GUID for the monitor.


## -remarks



In DirectX 9.0 and later, the monitor is identified by an integer index, not by a GUID.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

