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

# FDIIsCabinet function


## -description


The <b>FDIIsCabinet</b> function determines whether a file is a cabinet and, if it is, returns information about it.


## -parameters




### -param hfdi [in]

A valid FDI context handle returned  by <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>.


### -param hf [in]

An application-defined value to keep track of the opened file. This value must be of the same type as values used by the File I/O functions passed to <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>.


### -param pfdici [in, out]

Pointer to an <a href="https://msdn.microsoft.com/fde1a2ca-60cd-4a4d-9872-681e2f8f4fb1">FDICABINETINFO</a> structure that receives the cabinet details, in the event the file is actually a cabinet.


## -returns



If the file is a cabinet, the function returns <b>TRUE</b> ; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FDI context.




## -see-also




<a href="https://msdn.microsoft.com/fde1a2ca-60cd-4a4d-9872-681e2f8f4fb1">FDICABINETINFO</a>



<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>



<a href="https://msdn.microsoft.com/c923b0a5-1a8d-42aa-bd05-0d318199756d">FDITruncateCabinet</a>
 

 

