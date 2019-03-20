---
UID: NF:d3dcompiler.D3DCreateFunctionLinkingGraph
title: D3DCreateFunctionLinkingGraph function (d3dcompiler.h)
author: windows-sdk-content
description: Creates a function-linking-graph interface.
old-location: direct3dhlsl\d3dcreatefunctionlinkinggraph.htm
tech.root: direct3dhlsl
ms.assetid: D0BC7D62-EBF8-4144-8DC0-A87BF1B83006
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3DCreateFunctionLinkingGraph, D3DCreateFunctionLinkingGraph function [HLSL], d3dcompiler/D3DCreateFunctionLinkingGraph, direct3dhlsl.d3dcreatefunctionlinkinggraph
ms.topic: function
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
 - D3DCreateFunctionLinkingGraph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DCreateFunctionLinkingGraph function


## -description


Creates a function-linking-graph interface. <div class="alert"><b>Note</b>  This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>



## -parameters




### -param uFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Reserved


### -param ppFunctionLinkingGraph [out]

Type: <b><a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a> interface that is used for constructing shaders that consist of a sequence of precompiled function calls.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  The D3dcompiler_47.dll or later version of the DLL contains the <b>D3DCreateFunctionLinkingGraph</b> function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd607342(v=VS.85).aspx">Functions</a>



<a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>
 

 

