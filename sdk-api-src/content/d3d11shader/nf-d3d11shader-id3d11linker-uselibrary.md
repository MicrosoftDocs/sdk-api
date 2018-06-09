---
UID: NF:d3d11shader.ID3D11Linker.UseLibrary
title: ID3D11Linker::UseLibrary
author: windows-sdk-content
description: Adds an instance of a library module to be used for linking.
old-location: direct3d11\id3d11linker_uselibrary.htm
old-project: direct3d11
ms.assetid: 2FEA3583-8868-4763-8308-3C1E8F72A9BC
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11Linker interface [Direct3D 11],UseLibrary method, ID3D11Linker.UseLibrary, ID3D11Linker::UseLibrary, UseLibrary, UseLibrary method [Direct3D 11], UseLibrary method [Direct3D 11],ID3D11Linker interface, d3d11shader/ID3D11Linker::UseLibrary, direct3d11.id3d11linker_uselibrary
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_SHADER_VERSION_TYPE
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11Linker::UseLibrary


## -description


Adds an instance of a library module to be used for linking.


## -parameters




### -param pLibraryMI [in]

Type: <b><a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a> interface for the library module instance.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/08967A5F-AAAE-4352-A8A9-C7B1ED16EF25">ID3D11Linker</a>
 

 

