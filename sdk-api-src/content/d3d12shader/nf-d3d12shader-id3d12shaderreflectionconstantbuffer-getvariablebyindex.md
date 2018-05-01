---
UID: NF:d3d12shader.ID3D12ShaderReflectionConstantBuffer.GetVariableByIndex
title: ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex method
author: windows-driver-content
description: Gets a shader-reflection variable by index.
old-location: direct3d12\id3d12shaderreflectionconstantbuffer_getvariablebyindex.htm
old-project: direct3d12
ms.assetid: F7083A4D-ADD4-4C6F-A031-ABF16A3C351C
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetVariableByIndex method, GetVariableByIndex method, ID3D12ShaderReflectionConstantBuffer interface, GetVariableByIndex,ID3D12ShaderReflectionConstantBuffer.GetVariableByIndex, ID3D12ShaderReflectionConstantBuffer, ID3D12ShaderReflectionConstantBuffer interface, GetVariableByIndex method, ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex, d3d12shader/ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex, direct3d12.id3d12shaderreflectionconstantbuffer_getvariablebyindex
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12shader.h
api_name:
-	ID3D12ShaderReflectionConstantBuffer.GetVariableByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex method


## -description



          Gets a shader-reflection variable by index.
        


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Zero-based index.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable</a>*</b>


            A pointer to a shader-reflection variable interface (see <a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable Interface</a>).
          




## -remarks




        This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a>
 

 

