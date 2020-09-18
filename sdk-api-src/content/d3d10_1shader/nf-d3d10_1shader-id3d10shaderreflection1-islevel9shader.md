---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.IsLevel9Shader
title: ID3D10ShaderReflection1::IsLevel9Shader (d3d10_1shader.h)
description: Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.
helpviewer_keywords: ["ID3D10ShaderReflection1 interface [Direct3D 10]","IsLevel9Shader method","ID3D10ShaderReflection1.IsLevel9Shader","ID3D10ShaderReflection1::IsLevel9Shader","IsLevel9Shader","IsLevel9Shader method [Direct3D 10]","IsLevel9Shader method [Direct3D 10]","ID3D10ShaderReflection1 interface","d3d10_1shader/ID3D10ShaderReflection1::IsLevel9Shader","direct3d10.id3d10shaderreflection1_islevel9shader","eca068fc-c01b-15d4-2317-dbe4b6cf2b82"]
old-location: direct3d10\id3d10shaderreflection1_islevel9shader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_islevel9shader.htm
ms.date: 12/05/2018
ms.keywords: ID3D10ShaderReflection1 interface [Direct3D 10],IsLevel9Shader method, ID3D10ShaderReflection1.IsLevel9Shader, ID3D10ShaderReflection1::IsLevel9Shader, IsLevel9Shader, IsLevel9Shader method [Direct3D 10], IsLevel9Shader method [Direct3D 10],ID3D10ShaderReflection1 interface, d3d10_1shader/ID3D10ShaderReflection1::IsLevel9Shader, direct3d10.id3d10shaderreflection1_islevel9shader, eca068fc-c01b-15d4-2317-dbe4b6cf2b82
req.header: d3d10_1shader.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10ShaderReflection1::IsLevel9Shader
 - d3d10_1shader/ID3D10ShaderReflection1::IsLevel9Shader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1Shader.h
api_name:
 - ID3D10ShaderReflection1.IsLevel9Shader
---

# ID3D10ShaderReflection1::IsLevel9Shader


## -description

Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.

## -parameters

### -param pbLevel9Shader [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Pointer to a BOOL variable that will be set true if the shader was compiled in Direct3D 10 on Direct3D 9 mode; otherwise false.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/api/d3d10_1shader/nn-d3d10_1shader-id3d10shaderreflection1">ID3D10ShaderReflection1 Interface</a>