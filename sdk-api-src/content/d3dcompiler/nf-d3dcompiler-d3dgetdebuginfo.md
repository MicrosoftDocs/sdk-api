---
UID: NF:d3dcompiler.D3DGetDebugInfo
title: D3DGetDebugInfo function (d3dcompiler.h)
description: Note  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store. Gets shader debug information.
helpviewer_keywords: ["D3DGetDebugInfo","D3DGetDebugInfo function [HLSL]","d3dcompiler/D3DGetDebugInfo","direct3dhlsl.d3dgetdebuginfo","f21b6ffa-9910-4ce4-b2dc-07e7ad540fac"]
old-location: direct3dhlsl\d3dgetdebuginfo.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dgetdebuginfo.htm
ms.date: 12/05/2018
ms.keywords: D3DGetDebugInfo, D3DGetDebugInfo function [HLSL], d3dcompiler/D3DGetDebugInfo, direct3dhlsl.d3dgetdebuginfo, f21b6ffa-9910-4ce4-b2dc-07e7ad540fac
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DGetDebugInfo
 - d3dcompiler/D3DGetDebugInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DGetDebugInfo
---

# D3DGetDebugInfo function


## -description

<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Gets shader debug information.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to source data; either uncompiled or compiled HLSL code.

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pSrcData</i>.

### -param ppDebugInfo [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that contains debug information.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

Debug information is embedded in the body of the shader after calling <a href="/windows/desktop/direct3dhlsl/d3dcompile">D3DCompile</a>.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>