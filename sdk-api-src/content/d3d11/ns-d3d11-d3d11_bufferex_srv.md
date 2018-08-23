---
UID: NS:d3d11.D3D11_BUFFEREX_SRV
title: D3D11_BUFFEREX_SRV
author: windows-sdk-content
description: Describes the elements in a raw buffer resource to use in a shader-resource view.
old-location: direct3d11\d3d11_bufferex_srv.htm
old-project: direct3d11
ms.assetid: 55714c3b-ef21-43c1-94a1-60b63f3fedac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 6e2b4acb-42c7-1258-4812-425166fea83e, D3D11_BUFFEREX_SRV, D3D11_BUFFEREX_SRV structure [Direct3D 11], d3d11/D3D11_BUFFEREX_SRV, direct3d11.d3d11_bufferex_srv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_BUFFEREX_SRV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_BUFFEREX_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_BUFFEREX_SRV structure


## -description


Describes the elements in a raw buffer resource to use in a shader-resource view.


## -struct-fields




### -field FirstElement

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The index of the first element to be accessed by the view.


### -field NumElements

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of elements in the resource.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Ff476091(v=VS.85).aspx">D3D11_BUFFEREX_SRV_FLAG</a>-typed value that identifies view options for the buffer. Currently, the only option is to identify a raw view of the buffer. For more info about raw viewing of buffers, see <a href="https://msdn.microsoft.com/en-us/library/Ff476900(v=VS.85).aspx">Raw Views of Buffers</a>.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/en-us/library/Ff476211(v=VS.85).aspx">D3D11_SHADER_RESOURCE_VIEW_DESC</a> to create a raw view of a buffer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476173(v=VS.85).aspx">Resource Structures</a>
 

 

