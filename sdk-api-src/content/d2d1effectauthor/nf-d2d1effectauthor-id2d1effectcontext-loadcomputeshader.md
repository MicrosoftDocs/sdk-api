---
UID: NF:d2d1effectauthor.ID2D1EffectContext.LoadComputeShader
title: ID2D1EffectContext::LoadComputeShader
author: windows-sdk-content
description: Loads the given shader by its unique ID.
old-location: direct2d\id2d1contextinternal_loadcomputeshader.htm
tech.root: direct2d
ms.assetid: 64CA9647-8E9E-417D-A8D4-71AAF58F1C32
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID2D1EffectContext interface [Direct2D],LoadComputeShader method, ID2D1EffectContext.LoadComputeShader, ID2D1EffectContext::LoadComputeShader, LoadComputeShader, LoadComputeShader method [Direct2D], LoadComputeShader method [Direct2D],ID2D1EffectContext interface, d2d1effectauthor/ID2D1EffectContext::LoadComputeShader, direct2d.id2d1contextinternal_loadcomputeshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2D1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.LoadComputeShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::LoadComputeShader


## -description


Loads the given shader by its unique ID. Loading the shader multiple times is ignored. When the shader is loaded it is also handed to the driver to JIT, if it hasn’t been already.


## -parameters




### -param resourceId

Type: <b>REFGUID</b>

The unique id that identifies the shader.


### -param shaderBuffer

Type: <b>BYTE*</b>

The buffer that contains the shader to register.


### -param shaderBufferCount

Type: <b>UINT32</b>

The size of the shader buffer in bytes.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 




## -remarks



The shader you specify must be compiled,  not  in raw HLSL code.




## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

