---
UID: NF:d3dcompiler.D3DStripShader
title: D3DStripShader function
author: windows-driver-content
description: Removes unwanted blobs from a compilation result.
old-location: direct3dhlsl\d3dstripshader.htm
old-project: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dstripshader.htm
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: 3320d273-7542-f3d8-0828-2c357608a8c8, D3DStripShader, D3DStripShader function [HLSL], d3dcompiler/D3DStripShader, direct3dhlsl.d3dstripshader
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	D3DStripShader
product: Windows
targetos: Windows
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
---

# D3DStripShader function


## -description


Removes unwanted blobs from a compilation result.


## -parameters




### -param pShaderBytecode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to source data as compiled HLSL code.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pSrcData</i>.


### -param uStripFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Strip flag options, represented by <a href="https://msdn.microsoft.com/44e2af42-f5db-4206-aa00-37d070b2ca3b">D3DCOMPILER_STRIP_FLAGS</a>.


### -param ppStrippedBlob [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access the unwanted stripped out shader code.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

