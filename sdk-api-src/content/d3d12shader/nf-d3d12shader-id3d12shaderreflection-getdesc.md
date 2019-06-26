---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetDesc
title: ID3D12ShaderReflection::GetDesc (d3d12shader.h)
author: windows-sdk-content
description: Gets a shader description.
old-location: direct3d12\id3d12shaderreflection_getdesc.htm
tech.root: direct3d12
ms.assetid: D84DC99E-4E0C-4CFC-B061-FCD3C42D7937
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method, GetDesc method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetDesc method, ID3D12ShaderReflection.GetDesc, ID3D12ShaderReflection::GetDesc, d3d12shader/ID3D12ShaderReflection::GetDesc, direct3d12.id3d12shaderreflection_getdesc
ms.topic: method
f1_keywords: 
 - "d3d12shader/ID3D12ShaderReflection.GetDesc"
req.header: d3d12shader.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflection.GetDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12ShaderReflection::GetDesc


## -description


Gets a shader description.
        


## -parameters




### -param pDesc [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/ns-d3d12shader-_d3d12_shader_desc">D3D12_SHADER_DESC</a>*</b>

A shader description, as a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/ns-d3d12shader-_d3d12_shader_desc">D3D12_SHADER_DESC</a> structure.
          


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>
 

 

