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

# _D3D12_LIBRARY_DESC structure


## -description



          Describes a library.
        


## -struct-fields




### -field Creator


            The name of the originator of the library.
          


### -field Flags


            A combination of <a href="https://msdn.microsoft.com/039627DD-D6A4-4EA3-8E91-D2A20770E6FF">D3DCOMPILE Constants</a> that are combined by using a bitwise OR operation. The resulting value specifies how the compiler compiles.
          


### -field FunctionCount


            The number of functions exported from the library.
          


## -remarks




        This structure is returned by <a href="https://msdn.microsoft.com/BF7CC078-3F68-4645-B49C-1F4DEBCA6A48">ID3D12LibraryReflection::GetDesc</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/BF7CC078-3F68-4645-B49C-1F4DEBCA6A48">ID3D12LibraryReflection::GetDesc</a>



<a href="https://msdn.microsoft.com/b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0">Shader Structures</a>
 

 

