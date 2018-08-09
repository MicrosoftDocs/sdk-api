---
UID: NF:d3d10effect.D3D10DisassembleEffect
title: D3D10DisassembleEffect function
author: windows-sdk-content
description: This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use D3DDisassemble10Effect.
old-location: direct3d10\d3d10disassembleeffect.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10disassembleeffect.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 10ff0da2-3f88-22ec-7841-61c27051dfa6, D3D10DisassembleEffect, D3D10DisassembleEffect function [Direct3D 10], d3d10effect/D3D10DisassembleEffect, direct3d10.d3d10disassembleeffect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10effect.h
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10DisassembleEffect
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10DisassembleEffect function


## -description


This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use <a href="https://msdn.microsoft.com/fb6668ae-db7f-4d69-aed4-4b50f3a2b315">D3DDisassemble10Effect</a>.


## -parameters




### -param pEffect [in]

Type: <b><a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a>, which contains the compiled effect.


### -param EnableColorCode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Include HTML tags in the output to color code the result.


### -param ppDisassembly [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> which contains the disassembled shader.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.

Here is an example of disassembling a compiled effect. The example assumes you start with a compiled effect (shown as <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>l_pBlob_Effect</pre>
</td>
</tr>
</table></span></div> which you can see in <a href="https://msdn.microsoft.com/b8d8a0b7-b520-44e4-8691-6eb46202c092">Compile an Effect (Direct3D 10)</a>).

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleEffect( (UINT*) l_pBlob_Effect-&gt;GetBufferPointer(),
        l_pBlob_Effect-&gt;GetBufferSize(), TRUE, commentString, &amp;pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "effect.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly-&gt;GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b76643f0-387f-49c6-80e5-4d7b406b4db7">Effect Functions (Direct3D 10)</a>
 

 

