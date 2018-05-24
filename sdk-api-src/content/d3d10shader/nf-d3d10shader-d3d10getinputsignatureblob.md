---
UID: NF:d3d10shader.D3D10GetInputSignatureBlob
title: D3D10GetInputSignatureBlob function
author: windows-driver-content
description: Get a buffer that contains shader-input signatures.
old-location: direct3d10\d3d10getinputsignatureblob.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10getinputsignatureblob.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 127a7a10-b34d-1640-0c7f-282d07d86e4c, D3D10GetInputSignatureBlob, D3D10GetInputSignatureBlob function [Direct3D 10], d3d10shader/D3D10GetInputSignatureBlob, direct3d10.d3d10getinputsignatureblob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
-	DllExport
api_location:
-	D3D10.dll
api_name:
-	D3D10GetInputSignatureBlob
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10GetInputSignatureBlob function


## -description


Get a buffer that contains shader-input signatures.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="https://msdn.microsoft.com/cff6f901-cb9b-44d5-a75b-9a4029a37215">Getting a Pointer to a Compiled Shader</a>.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The size of the shader bytecode in bytes.


### -param ppSignatureBlob [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

The address of a pointer to the buffer (see <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>



<a href="https://msdn.microsoft.com/c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32">Shader Functions</a>
 

 

