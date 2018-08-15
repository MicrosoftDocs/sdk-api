---
UID: NF:d3d11shader.ID3D11Linker.AddClipPlaneFromCBuffer
title: ID3D11Linker::AddClipPlaneFromCBuffer
author: windows-sdk-content
description: Adds a clip plane with the plane coefficients taken from a cbuffer entry for 10Level9 shaders.
old-location: direct3d11\id3d11linker_addclipplanefromcbuffer.htm
old-project: direct3d11
ms.assetid: 0E7820F1-8F4E-43B2-A8DD-560BC2B5BC3D
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddClipPlaneFromCBuffer, AddClipPlaneFromCBuffer method [Direct3D 11], AddClipPlaneFromCBuffer method [Direct3D 11],ID3D11Linker interface, ID3D11Linker interface [Direct3D 11],AddClipPlaneFromCBuffer method, ID3D11Linker.AddClipPlaneFromCBuffer, ID3D11Linker::AddClipPlaneFromCBuffer, d3d11shader/ID3D11Linker::AddClipPlaneFromCBuffer, direct3d11.id3d11linker_addclipplanefromcbuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11shader.h
req.include-header: 
req.redist: 
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11Linker.AddClipPlaneFromCBuffer
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11Linker::AddClipPlaneFromCBuffer


## -description


Adds a <a href="https://msdn.microsoft.com/C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11">clip plane</a> with the plane coefficients taken from a <a href="https://msdn.microsoft.com/en-us/library/Bb509581(v=VS.85).aspx">cbuffer</a> entry for 10Level9 shaders.


## -parameters




### -param uCBufferSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb509581(v=VS.85).aspx">cbuffer</a> slot number.


### -param uCBufferEntry [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb509581(v=VS.85).aspx">cbuffer</a> entry number.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/08967A5F-AAAE-4352-A8A9-C7B1ED16EF25">ID3D11Linker</a>
 

 

