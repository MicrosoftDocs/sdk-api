---
UID: NF:d3d11shader.ID3D11Linker.UseLibrary
title: ID3D11Linker::UseLibrary
author: windows-sdk-content
description: Adds an instance of a library module to be used for linking.
old-location: direct3d11\id3d11linker_uselibrary.htm
tech.root: direct3d11
ms.assetid: 2FEA3583-8868-4763-8308-3C1E8F72A9BC
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11Linker interface [Direct3D 11],UseLibrary method, ID3D11Linker.UseLibrary, ID3D11Linker::UseLibrary, UseLibrary, UseLibrary method [Direct3D 11], UseLibrary method [Direct3D 11],ID3D11Linker interface, d3d11shader/ID3D11Linker::UseLibrary, direct3d11.id3d11linker_uselibrary
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
 - ID3D11Linker.UseLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Linker::UseLibrary


## -description


Adds an instance of a library module to be used for linking.


## -parameters




### -param pLibraryMI [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn280564(v=VS.85).aspx">ID3D11ModuleInstance</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn280564(v=VS.85).aspx">ID3D11ModuleInstance</a> interface for the library module instance.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280558(v=VS.85).aspx">ID3D11Linker</a>
 

 

