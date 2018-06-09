---
UID: NS:d3d12shader._D3D12_LIBRARY_DESC
title: "_D3D12_LIBRARY_DESC"
author: windows-sdk-content
description: Describes a library.
old-location: direct3d12\d3d12_library_desc.htm
old-project: direct3d12
ms.assetid: 99CB0B61-8494-4591-A3CB-B6DAD19C79ED
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: D3D12_LIBRARY_DESC, D3D12_LIBRARY_DESC structure, _D3D12_LIBRARY_DESC, d3d12shader/D3D12_LIBRARY_DESC, direct3d12.d3d12_library_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12shader.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: D3D12_LIBRARY_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12shader.h
api_name:
 - D3D12_LIBRARY_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

