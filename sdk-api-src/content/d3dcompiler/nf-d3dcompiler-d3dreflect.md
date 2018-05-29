---
UID: NF:d3dcompiler.D3DReflect
title: D3DReflect function
author: windows-sdk-content
description: Gets a pointer to a reflection interface.
old-location: direct3dhlsl\d3dreflect.htm
old-project: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dreflect.htm
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: 3df99cee-b0b6-2f29-2bd1-7eb53e907191, D3DReflect, D3DReflect function [HLSL], d3dcompiler/D3DReflect, direct3dhlsl.d3dreflect
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: D3D_BLOB_PART
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	d3dcompiler_47.dll
api_name:
-	D3DReflect
product: Windows
targetos: Windows
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
---

# D3DReflect function


## -description


Gets a pointer to a reflection interface.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to source data as compiled HLSL code.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pSrcData</i>.


### -param pInterface [in]

Type: <b>REFIID</b>

The reference GUID of the COM interface to use. For example, <b>IID_ID3D11ShaderReflection</b>.


### -param ppReflector [out]

Type: <b>void**</b>

A pointer to a reflection interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



Shader code contains metadata that can be inspected using the reflection APIs.

The following code illustrates retrieving a <a href="https://msdn.microsoft.com/a28cca72-7f2d-416a-bfa9-4d1f71fc98d5">ID3D11ShaderReflection</a> Interface from a shader.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
pd3dDevice-&gt;CreatePixelShader( pPixelShaderBuffer-&gt;GetBufferPointer(),
                               pPixelShaderBuffer-&gt;GetBufferSize(), g_pPSClassLinkage, &amp;g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3DReflect( pPixelShaderBuffer-&gt;GetBufferPointer(), pPixelShaderBuffer-&gt;GetBufferSize(), 
            IID_ID3D11ShaderReflection, (void**) &amp;pReflector);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

