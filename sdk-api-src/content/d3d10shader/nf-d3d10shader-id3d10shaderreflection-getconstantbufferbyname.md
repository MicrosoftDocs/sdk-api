---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetConstantBufferByName
title: ID3D10ShaderReflection::GetConstantBufferByName
author: windows-driver-content
description: Get a constant buffer by name.
old-location: direct3d10\id3d10shaderreflection_getconstantbufferbyname.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getconstantbufferbyname.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method [Direct3D 10], GetConstantBufferByName method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetConstantBufferByName method, ID3D10ShaderReflection.GetConstantBufferByName, ID3D10ShaderReflection::GetConstantBufferByName, c597f147-5514-438b-1e81-09771d342a5f, d3d10shader/ID3D10ShaderReflection::GetConstantBufferByName, direct3d10.id3d10shaderreflection_getconstantbufferbyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10shader.h
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
req.typenames: D3D10_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Shader.h
api_name:
-	ID3D10ShaderReflection.GetConstantBufferByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection::GetConstantBufferByName


## -description


Get a constant buffer by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The constant-buffer name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/5418147a-6d9f-44fc-a9ce-f619fc389ee4">ID3D10ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="https://msdn.microsoft.com/5418147a-6d9f-44fc-a9ce-f619fc389ee4">ID3D10ShaderReflectionConstantBuffer Interface</a>).




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.




## -see-also




<a href="https://msdn.microsoft.com/097ed643-4e7a-4214-80a1-9a56d1157044">ID3D10ShaderReflection Interface</a>
 

 

