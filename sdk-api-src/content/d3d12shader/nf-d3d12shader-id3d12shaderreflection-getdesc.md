---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetDesc
title: ID3D12ShaderReflection::GetDesc
author: windows-sdk-content
description: Gets a shader description.
old-location: direct3d12\id3d12shaderreflection_getdesc.htm
old-project: direct3d12
ms.assetid: D84DC99E-4E0C-4CFC-B061-FCD3C42D7937
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetDesc, GetDesc method, GetDesc method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetDesc method, ID3D12ShaderReflection.GetDesc, ID3D12ShaderReflection::GetDesc, d3d12shader/ID3D12ShaderReflection::GetDesc, direct3d12.id3d12shaderreflection_getdesc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D12_SHADER_VERSION_TYPE
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
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflection::GetDesc


## -description


Gets a shader description.
        


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/FE989434-B1B6-48F3-8F95-64B1E7C988F5">D3D12_SHADER_DESC</a>*</b>

A shader description, as a pointer to a <a href="https://msdn.microsoft.com/FE989434-B1B6-48F3-8F95-64B1E7C988F5">D3D12_SHADER_DESC</a> structure.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

