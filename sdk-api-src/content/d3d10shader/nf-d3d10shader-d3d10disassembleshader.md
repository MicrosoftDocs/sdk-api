---
UID: NF:d3d10shader.D3D10DisassembleShader
title: D3D10DisassembleShader function
author: windows-sdk-content
description: This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use D3DDisassemble.
old-location: direct3d10\d3d10disassembleshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10disassembleshader.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 3e4c4f2f-1754-2bbc-636d-9cea485ffad1, D3D10DisassembleShader, D3D10DisassembleShader function [Direct3D 10], d3d10shader/D3D10DisassembleShader, direct3d10.d3d10disassembleshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10shader.h
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
req.typenames: D3D10_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10DisassembleShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10DisassembleShader function


## -description


This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use <a href="https://msdn.microsoft.com/0b5cfe31-1277-4923-a6e2-7e020019b74c">D3DDisassemble</a>.


## -parameters




### -param pShader [in]

Type: <b>const void*</b>

A pointer to the compiled shader.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The size of pShader.


### -param EnableColorCode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Include HTML tags in the output to color code the result.


### -param pComments [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The comment string at the top of the shader that identifies the shader constants and variables.


### -param ppDisassembly [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

Address of a buffer which contains the disassembled shader.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Return value




## -see-also




<a href="https://msdn.microsoft.com/c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32">Shader Functions</a>
 

 

