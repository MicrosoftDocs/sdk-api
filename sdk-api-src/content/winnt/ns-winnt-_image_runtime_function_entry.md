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

# _IMAGE_RUNTIME_FUNCTION_ENTRY structure


## -description


Represents an entry in the function table on 64-bit Windows.


## -struct-fields




### -field BeginAddress

The address of the start of the function.


### -field EndAddress

The address of the end of the function.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.UnwindInfoAddress

The address of the unwind information for the function.


### -field DUMMYUNIONNAME.UnwindData

 




## -see-also




<a href="https://msdn.microsoft.com/f79e6af9-9931-4bd7-ae12-29d890267a89">SymFunctionTableAccess64</a>
 

 

