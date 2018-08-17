---
UID: NF:d3d11.ID3D11DeviceContext.IASetIndexBuffer
title: ID3D11DeviceContext::IASetIndexBuffer
author: windows-sdk-content
description: Bind an index buffer to the input-assembler stage.
old-location: direct3d11\id3d11devicecontext_iasetindexbuffer.htm
old-project: direct3d11
ms.assetid: c556dda2-0808-4701-90cb-16c67a24add1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 73896724-c6e5-3a60-25c3-af31308264c5, IASetIndexBuffer, IASetIndexBuffer method [Direct3D 11], IASetIndexBuffer method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IASetIndexBuffer method, ID3D11DeviceContext.IASetIndexBuffer, ID3D11DeviceContext::IASetIndexBuffer, d3d11/ID3D11DeviceContext::IASetIndexBuffer, direct3d11.id3d11devicecontext_iasetindexbuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.IASetIndexBuffer
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::IASetIndexBuffer


## -description


Bind an index buffer to the input-assembler stage.


## -parameters




### -param pIndexBuffer [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a> object, that contains indices. The index buffer must have been created with
            the <a href="https://msdn.microsoft.com/en-us/library/Ff476085(v=VS.85).aspx">D3D11_BIND_INDEX_BUFFER</a> flag.
          


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> that specifies the format of the data in the index buffer. The only formats allowed for index
            buffer data are 16-bit (DXGI_FORMAT_R16_UINT) and 32-bit (DXGI_FORMAT_R32_UINT) integers.
          


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Offset (in bytes) from the start of the index buffer to the first index to use.


## -returns



Returns nothing.




## -remarks



For information about creating index buffers, see <a href="https://msdn.microsoft.com/en-us/library/Ff476897(v=VS.85).aspx">How to: Create an Index Buffer</a>.
        

Calling this method using a buffer that is currently bound for writing (i.e. bound to the stream output pipeline stage) will effectively bind
          <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.
        

The debug layer will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will
          not prevent invalid data from being used by the runtime.
        

The method will hold a reference to the interfaces passed in.
          This differs from the device state behavior in Direct3D 10.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

