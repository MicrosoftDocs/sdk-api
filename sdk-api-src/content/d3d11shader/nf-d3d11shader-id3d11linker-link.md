---
UID: NF:d3d11shader.ID3D11Linker.Link
title: ID3D11Linker::Link
author: windows-sdk-content
description: Links the shader and produces a shader blob that the Direct3D runtime can use.
old-location: direct3d11\id3d11linker_link.htm
tech.root: direct3d11
ms.assetid: FCEAE5C2-38E4-4B8F-BA98-F46B187FC586
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11Linker interface [Direct3D 11],Link method, ID3D11Linker.Link, ID3D11Linker::Link, Link, Link method [Direct3D 11], Link method [Direct3D 11],ID3D11Linker interface, d3d11shader/ID3D11Linker::Link, direct3d11.id3d11linker_link
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11Linker.Link
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Linker::Link


## -description


Links the shader and produces a shader blob that the Direct3D runtime can use.
        


## -parameters




### -param pEntry [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn280564(v=VS.85).aspx">ID3D11ModuleInstance</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn280564(v=VS.85).aspx">ID3D11ModuleInstance</a> interface for the shader module instance to link from.
          


### -param pEntryName [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The name of the shader module instance to link from.
          


### -param pTargetName [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The name for the shader blob that is produced.
          


### -param uFlags [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Reserved.
          


### -param ppShaderBlob [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access the compiled shader code.
          


### -param ppErrorBuffer [out, optional]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access compiler error messages.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280558(v=VS.85).aspx">ID3D11Linker</a>
 

 

