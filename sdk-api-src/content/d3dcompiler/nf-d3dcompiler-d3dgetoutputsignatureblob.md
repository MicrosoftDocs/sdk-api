---
UID: NF:d3dcompiler.D3DGetOutputSignatureBlob
title: D3DGetOutputSignatureBlob function
author: windows-sdk-content
description: Note  D3DGetOutputSignatureBlob may be altered or unavailable for releases after Windows 8.1. Instead use D3DGetBlobPart with the D3D_BLOB_OUTPUT_SIGNATURE_BLOB value.  Gets the output signature from a compilation result.
old-location: direct3dhlsl\d3dgetoutputsignatureblob.htm
old-project: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dgetoutputsignatureblob.htm
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: 7e5f0af9-0b60-521e-b5f2-72b0c89909a0, D3DGetOutputSignatureBlob, D3DGetOutputSignatureBlob function [HLSL], d3dcompiler/D3DGetOutputSignatureBlob, direct3dhlsl.d3dgetoutputsignatureblob
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
tech.root: 
req.typenames: D3D_BLOB_PART
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DGetOutputSignatureBlob
product: Windows
targetos: Windows
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
---

# D3DGetOutputSignatureBlob function


## -description


<div class="alert"><b>Note</b>  <b>D3DGetOutputSignatureBlob</b> may be altered or unavailable for releases after Windows 8.1. Instead use <a href="https://msdn.microsoft.com/cf9cea53-e7a3-4473-bfdf-0cdeb8370974">D3DGetBlobPart</a> with the <a href="/windows/desktop/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part">D3D_BLOB_OUTPUT_SIGNATURE_BLOB</a> value. </div><div> </div>Gets the output signature from a compilation result.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to source data as compiled HLSL code.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pSrcData</i>.


### -param ppSignatureBlob [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that contains a compiled shader.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

