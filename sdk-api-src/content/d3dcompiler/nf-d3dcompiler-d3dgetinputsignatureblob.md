---
UID: NF:d3dcompiler.D3DGetInputSignatureBlob
title: D3DGetInputSignatureBlob function (d3dcompiler.h)
author: windows-sdk-content
description: Note  D3DGetInputSignatureBlob may be altered or unavailable for releases after Windows 8.1. Instead use D3DGetBlobPart with the D3D_BLOB_INPUT_SIGNATURE_BLOB value.  Gets the input signature from a compilation result.
old-location: direct3dhlsl\d3dgetinputsignatureblob.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dgetinputsignatureblob.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 4f2b8180-4af5-06c2-bd88-b229e19ce686, D3DGetInputSignatureBlob, D3DGetInputSignatureBlob function [HLSL], d3dcompiler/D3DGetInputSignatureBlob, direct3dhlsl.d3dgetinputsignatureblob
ms.topic: function
f1_keywords: 
 - "d3dcompiler/D3DGetInputSignatureBlob"
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
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DGetInputSignatureBlob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# D3DGetInputSignatureBlob function


## -description


<div class="alert"><b>Note</b>  <b>D3DGetInputSignatureBlob</b> may be altered or unavailable for releases after Windows 8.1. Instead use <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/d3dgetblobpart">D3DGetBlobPart</a> with the <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/d3d-blob-part">D3D_BLOB_INPUT_SIGNATURE_BLOB</a> value. </div><div> </div>Gets the input signature from a compilation result.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to source data as compiled HLSL code.


### -param SrcDataSize [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pSrcData</i>.


### -param ppSignatureBlob [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that contains a compiled shader.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>
 

 

