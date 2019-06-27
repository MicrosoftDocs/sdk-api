---
UID: NF:d3dcompiler.D3DReflectLibrary
title: D3DReflectLibrary function (d3dcompiler.h)
author: windows-sdk-content
description: Creates a library-reflection interface from source data that contains an HLSL library of functions.
old-location: direct3dhlsl\d3dreflectlibrary.htm
tech.root: direct3dhlsl
ms.assetid: E64FB2C3-8F64-411F-89E1-984DAAE4D7C2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3DReflectLibrary, D3DReflectLibrary function [HLSL], d3dcompiler/D3DReflectLibrary, direct3dhlsl.d3dreflectlibrary
ms.topic: function
f1_keywords: 
 - "d3dcompiler/D3DReflectLibrary"
req.header: d3dcompiler.h
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
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DReflectLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# D3DReflectLibrary function


## -description


Creates a library-reflection interface from source data that contains an HLSL library of functions. <div class="alert"><b>Note</b>  This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>



## -parameters




### -param pSrcData [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to source data as an HLSL library of functions. 


### -param SrcDataSize [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.


### -param riid [in]

Type: <b>REFIID</b>

The reference GUID of the COM interface to use. For example, <b>IID_ID3D11LibraryReflection</b>.


### -param ppReflector [out]

Type: <b>LPVOID*</b>

A pointer to a variable that receives a pointer to a library-reflection interface, <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11libraryreflection">ID3D11LibraryReflection</a>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11libraryreflection">ID3D11LibraryReflection</a>
 

 

