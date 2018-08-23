---
UID: NS:d3d11shader._D3D11_LIBRARY_DESC
title: "_D3D11_LIBRARY_DESC"
author: windows-sdk-content
description: Describes a library.
old-location: direct3d11\d3d11_library_desc.htm
old-project: direct3d11
ms.assetid: A4AC9733-DB17-4855-AEB0-3DA7819F6627
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D11_LIBRARY_DESC, D3D11_LIBRARY_DESC structure [Direct3D 11], _D3D11_LIBRARY_DESC, d3d11shader/D3D11_LIBRARY_DESC, direct3d11.d3d11_library_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11shader.h
req.include-header: 
req.redist: 
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
req.typenames: D3D11_LIBRARY_DESC
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
req.lib: 
req.dll: 
req.irql: 
---

# _D3D11_LIBRARY_DESC structure


## -description


Describes a library.


## -struct-fields




### -field Creator

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The name of the originator of the library.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/en-us/library/Gg615083(v=VS.85).aspx">D3DCOMPILE Constants</a> that are combined by using a bitwise OR operation. The resulting value specifies how the compiler compiles.


### -field FunctionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of functions exported from the library.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280556(v=VS.85).aspx">ID3D11LibraryReflection::GetDesc</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476176(v=VS.85).aspx">Shader Structures</a>
 

 

