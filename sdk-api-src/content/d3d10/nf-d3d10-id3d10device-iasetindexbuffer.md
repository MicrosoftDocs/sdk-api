---
UID: NF:d3d10.ID3D10Device.IASetIndexBuffer
title: ID3D10Device::IASetIndexBuffer
author: windows-sdk-content
description: Bind an index buffer to the input-assembler stage.
old-location: direct3d10\id3d10device_iasetindexbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iasetindexbuffer.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 608d16ec-f6d6-ea93-bc37-fe7d34d07215, IASetIndexBuffer, IASetIndexBuffer method [Direct3D 10], IASetIndexBuffer method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IASetIndexBuffer method, ID3D10Device.IASetIndexBuffer, ID3D10Device::IASetIndexBuffer, d3d10/ID3D10Device::IASetIndexBuffer, direct3d10.id3d10device_iasetindexbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.IASetIndexBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.IASetIndexBuffer
: 
---

# ID3D10Device::IASetIndexBuffer


## -description


Bind an <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">index buffer</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler</a> stage.


## -parameters




### -param pIndexBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>*</b>

A pointer to a buffer (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>) that contains indices. The index buffer must have been created with the <a href="https://msdn.microsoft.com/en-us/library/Bb204891(v=VS.85).aspx">D3D10_BIND_INDEX_BUFFER</a> flag.


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

Specifies format of the data in the index buffer. The only formats allowed for index buffer data are 16-bit (<a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_R16_UINT</a>) and 32-bit (<b>DXGI_FORMAT_R32_UINT</b>) integers.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset (in bytes) from the start of the index buffer to the first index to use.


## -returns



Returns nothing.




## -remarks



For information about creating index buffers, see <a href="https://msdn.microsoft.com/en-us/library/Bb205130(v=VS.85).aspx">Create an Index Buffer</a>.

Calling this method using a buffer that is currently bound for writing (i.e. bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205121(v=VS.85).aspx">stream output</a> pipeline stage) will effectively bind <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.

The <a href="https://msdn.microsoft.com/en-us/library/Bb205068(v=VS.85).aspx">Debug Layer</a> will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

