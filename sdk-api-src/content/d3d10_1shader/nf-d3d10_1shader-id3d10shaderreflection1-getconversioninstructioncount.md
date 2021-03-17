---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.GetConversionInstructionCount
title: ID3D10ShaderReflection1::GetConversionInstructionCount (d3d10_1shader.h)
description: Gets the number of conversion instructions used in a shader.
helpviewer_keywords: ["GetConversionInstructionCount","GetConversionInstructionCount method [Direct3D 10]","GetConversionInstructionCount method [Direct3D 10]","ID3D10ShaderReflection1 interface","ID3D10ShaderReflection1 interface [Direct3D 10]","GetConversionInstructionCount method","ID3D10ShaderReflection1.GetConversionInstructionCount","ID3D10ShaderReflection1::GetConversionInstructionCount","d3d10_1shader/ID3D10ShaderReflection1::GetConversionInstructionCount","direct3d10.id3d10shaderreflection1_getconversioninstructioncount","f8c14b46-5062-b621-c098-57fd31ed02ea"]
old-location: direct3d10\id3d10shaderreflection1_getconversioninstructioncount.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_getconversioninstructioncount.htm
ms.date: 12/05/2018
ms.keywords: GetConversionInstructionCount, GetConversionInstructionCount method [Direct3D 10], GetConversionInstructionCount method [Direct3D 10],ID3D10ShaderReflection1 interface, ID3D10ShaderReflection1 interface [Direct3D 10],GetConversionInstructionCount method, ID3D10ShaderReflection1.GetConversionInstructionCount, ID3D10ShaderReflection1::GetConversionInstructionCount, d3d10_1shader/ID3D10ShaderReflection1::GetConversionInstructionCount, direct3d10.id3d10shaderreflection1_getconversioninstructioncount, f8c14b46-5062-b621-c098-57fd31ed02ea
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
 - ID3D10ShaderReflection1::GetConversionInstructionCount
 - d3d10_1shader/ID3D10ShaderReflection1::GetConversionInstructionCount
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
 - ID3D10ShaderReflection1.GetConversionInstructionCount
---

# ID3D10ShaderReflection1::GetConversionInstructionCount


## -description

Gets the number of conversion instructions used in a shader.

## -parameters

### -param pCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a UINT that will contain the conversion instruction count when the method returns.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/api/d3d10_1shader/nn-d3d10_1shader-id3d10shaderreflection1">ID3D10ShaderReflection1 Interface</a>