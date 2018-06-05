---
UID: NF:d3d12.ID3D12GraphicsCommandList.IASetVertexBuffers
title: ID3D12GraphicsCommandList::IASetVertexBuffers
author: windows-sdk-content
description: Sets a CPU descriptor handle for the vertex buffers.
old-location: direct3d12\id3d12graphicscommandlist_iasetvertexbuffers.htm
old-project: direct3d12
ms.assetid: AADD6CEF-376D-43AB-86E6-37B5D7DD0B25
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IASetVertexBuffers, IASetVertexBuffers method, IASetVertexBuffers method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,IASetVertexBuffers method, ID3D12GraphicsCommandList.IASetVertexBuffers, ID3D12GraphicsCommandList::IASetVertexBuffers, d3d12/ID3D12GraphicsCommandList::IASetVertexBuffers, direct3d12.id3d12graphicscommandlist_iasetvertexbuffers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12.dll
api_name:
-	ID3D12GraphicsCommandList.IASetVertexBuffers
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::IASetVertexBuffers


## -description


Sets a CPU descriptor handle for the vertex buffers.


## -parameters




### -param StartSlot [in]

Type: <b>UINT</b>


            Index into the device's zero-based array to begin setting vertex buffers.
          


### -param NumViews [in]

Type: <b>UINT</b>


            The number of views in the <i>pViews</i> array.
          


### -param pViews [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/7EFE1929-FCDD-48DD-99E4-135D8B515290">D3D12_VERTEX_BUFFER_VIEW</a>*</b>


            Specifies the vertex buffer views in an array of <a href="https://msdn.microsoft.com/7EFE1929-FCDD-48DD-99E4-135D8B515290">D3D12_VERTEX_BUFFER_VIEW</a> structures.
          


## -returns




            This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/EB776EC7-42F2-47D3-A1FA-771EC6C4E3AB">IASetIndexBuffer</a>



<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

