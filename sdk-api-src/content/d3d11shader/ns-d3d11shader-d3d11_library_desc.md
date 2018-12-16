---
UID: NS:d3d11shader._D3D11_LIBRARY_DESC
title: D3D11_LIBRARY_DESC
author: windows-sdk-content
description: Describes a library.
old-location: direct3d11\d3d11_library_desc.htm
tech.root: direct3d11
ms.assetid: A4AC9733-DB17-4855-AEB0-3DA7819F6627
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_LIBRARY_DESC, D3D11_LIBRARY_DESC structure [Direct3D 11], d3d11shader/D3D11_LIBRARY_DESC, direct3d11.d3d11_library_desc
ms.topic: struct
req.header: d3d11shader.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
api_name:
 - D3D11_LIBRARY_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_LIBRARY_DESC
req.redist: 
---

# D3D11_LIBRARY_DESC structure


## -description


Describes a library.


## -struct-fields




### -field Creator

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the originator of the library.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/039627DD-D6A4-4EA3-8E91-D2A20770E6FF">D3DCOMPILE Constants</a> that are combined by using a bitwise OR operation. The resulting value specifies how the compiler compiles.


### -field FunctionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of functions exported from the library.


## -see-also




<a href="https://msdn.microsoft.com/F23FEED8-94A3-4A87-8B4F-1D55BD47AF5F">ID3D11LibraryReflection::GetDesc</a>



<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

