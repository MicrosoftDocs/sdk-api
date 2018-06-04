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

# RtlLookupFunctionEntry function


## -description


Searches the active function tables for an entry that corresponds to the specified PC 
   value.


## -parameters




### -param ControlPc [in]

The virtual address of an instruction bundle within the function.


### -param ImageBase [out]

The base address of module to which the function belongs.


### -param HistoryTable

TBD




#### - TargetGp [out]

The global pointer value of the module.

This parameter has a different declaration on x64 and ARM systems. For more information, see x64 Definition 
        and ARM Definition.


## -returns



If there is no entry in the function table for the specified PC, the function returns 
      <b>NULL</b>. Otherwise, the function returns the address of the function table entry that 
      corresponds to the specified PC.




## -see-also




<a href="https://msdn.microsoft.com/3d2d8778-311e-4cc1-b280-4f83ab457755">RtlUnwindEx</a>



<a href="https://msdn.microsoft.com/78d60f7a-0e16-4856-8aca-c251ab066b83">RtlVirtualUnwind</a>
 

 

